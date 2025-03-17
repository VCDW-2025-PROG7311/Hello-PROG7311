
## Creating an MVC Web App
After creating a MVC Web App in .NET (no auth, no docker). Run you app and check it runs ok.

## Connecting the App to the DB

Using the following commands in the Developer Command Prompt, connect the app to your DB. You need to cd into your project folder.

1. Install dotnet-ef
    ```
    dotnet tool install --global dotnet-ef
    ```

2. Install these packages:
    ```
    dotnet add package Microsoft.EntityFrameworkCore.Design 
    dotnet add package Microsoft.EntityFrameworkCore.SqlServer
    ```

3. Run the scaffold command, after adjusting for your server and database:
    ```
    dotnet ef dbcontext scaffold "Server={your SQL server name};Database={your db name};Trusted_Connection=True;TrustServerCertificate=True;" Microsoft.EntityFrameworkCore.SqlServer -o Models
    ```

4. Once the model is created, you will need to move the connection string out of the context class into appsetting.json and will need to setup the service in Program.cs.
 
    Remove the following from the DB context class:
    ```
    protected override void OnConfiguring(DbContextOptionsBuilder optionsBuilder)
    #warning To protect potentially sensitive information in your connection string, you should move it out of source code. You can avoid scaffolding the connection string by using the Name= syntax to read it from configuration - see https://go.microsoft.com/fwlink/?linkid=2131148. For more guidance on storing connection strings, see https://go.microsoft.com/fwlink/?LinkId=723263.
            => optionsBuilder.UseSqlServer("Server={your SQL server name};Database={your db name};Trusted_Connection=True;TrustServerCertificate=True;");
    ```

### Adding the Connection String in Environment variables - OPTION 1

1. Add the connection string for your SQL Server inside a system-wide environment variable named `{your env variable name}`. This will need some research.

2. Add the following code to your Program.cs class after `builder.Services.AddControllersWithViews();`:
    ```
    builder.Services.AddDbContext<MathDbContext>(options =>
                    options.UseSqlServer(Environment.GetEnvironmentVariable("{your env variable name}")));
    ```

### Adding Connection String in appsettings.json - OPTION 2

1. Add the following section to your appsettings.json (remember to update):
    ```
      "ConnectionStrings": {
        "{your env variable name}": "{your connection string}"
      },
    ```

1. Add the following code to your Program.cs class after `builder.Services.AddControllersWithViews();`:
    ```
    builder.Services.AddDbContext<MathDbContext>(options =>
                    options.UseSqlServer(builder.Configuration.GetConnectionString("{your env variable name}")));
    ```


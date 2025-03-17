## Freelancer App - Weekly Plan and Instructions

### Overview
Over the next 6 weeks, you (individually or in pairs) will build a Freelancing Platform (mine is called Freelancer, but you can call yours whatever you want to) using ASP.NET Core MVC, Web API, EF Core, Firebase, PayFast, SendGrid, Docker, and CircleCI.  

This project will help you develop full-stack development skills, including database design, backend API development, frontend implementation, authentication, payments, email notifications, and CI/CD deployment.

---

### Week 1: Project Planning and Database Setup
#### Objectives:
- Understand project requirements
- Create an architecture diagram
- Design the database schema (ERD)
- Set up SQL Server and define tables
- Configure Entity Framework Core and apply migrations

#### Tasks:
1. Define functional and non-functional requirements for the app.
2. Create an architecture diagram outlining system components.
3. Design an ERD for Freelancers, Customers, Bookings, Payments, and Reviews.
4. Write SQL scripts to create database tables.
5. Set up an ASP.NET Core MVC project and integrate Entity Framework Core.
6. Apply migrations to generate the database.

---

### Week 2: Building the MVC Web Application
#### Objectives:
- Implement the frontend using ASP.NET Core MVC
- Set up Razor views for Freelancer listings
- Implement CRUD operations using the repository pattern
- Connect the frontend to the database

#### Tasks:
1. Create the UI for Freelancer listings and customer registration.
2. Implement CRUD operations for Freelancers and Customers.
3. Display data from the database in the UI.
4. Ensure views are dynamic and respond to database updates.

---

### Week 3: Splitting the App into API and Frontend
#### Objectives:
- Develop an ASP.NET Core Web API
- Implement DTOs and AutoMapper
- Secure API using Firebase Authentication
- Update the MVC app to consume the API

#### Tasks:
1. Create API controllers for Freelancers, Customers, and Bookings.
2. Implement DTOs to format API responses properly.
3. Secure API endpoints using Firebase Authentication.
4. Modify the frontend to interact with the API.

---

### Week 4: Booking and Payment Integration
#### Objectives:
- Implement booking functionality
- Integrate PayFast for payments
- Handle payment callbacks and store transactions
- Write unit tests for booking and payment services

#### Tasks:
1. Implement the booking API where customers can book freelancers.
2. Integrate PayFast to handle payments.
3. Store and log transactions after successful payments.
4. Ensure proper validation for booking and payment processing.

---

### Week 5: Email Notifications and Dockerization
#### Objectives:
- Implement SendGrid for email notifications
- Send emails when bookings are confirmed
- Dockerize API and frontend
- Write Docker Compose files for a multi-container setup

#### Tasks:
1. Set up SendGrid and configure it for email notifications.
2. Send confirmation emails when a booking is successfully completed.
3. Dockerize the API and frontend for containerized deployment.
4. Test Docker containers locally.

---

### Week 6: Deployment and Enhancements
#### Objectives:
- Set up CI/CD pipeline with CircleCI
- Deploy API and frontend to a cloud platform
- Implement monitoring and logging
- Enhance the app with extra features (e.g., freelancer reviews)

#### Tasks:
1. Configure a CircleCI pipeline for automated deployment.
2. Deploy the application to DigitalOcean, Azure, or AWS.
3. Set up logging and monitoring for API and frontend.
4. Implement an additional feature, such as freelancer reviews.

---

### Final Outcome:
At the end of Week 6, you will have:
- A fully functional full-stack Freelancer app  
- GitHub repository with clean, well-documented code  
- Final report with reflections on the project  
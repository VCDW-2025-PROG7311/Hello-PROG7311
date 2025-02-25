# 📝 Implementing the Memento Design Pattern for a Text Editor

## 📌 Scenario:  
You are developing a **simple text editor** in a .NET MVC application. The text editor should allow users to **enter text**, **save the current state**, and **undo changes** to revert to the previously saved state. To achieve this, you must implement the **Memento Design Pattern**, which will separate concerns between storing, restoring, and managing text states.

## ✅ Requirements:  
1. **Create a class `TextEditorMemento`** that represents the saved state of the text.
2. **Implement an `Originator` class called `TextEditor`** that:
   - Has a property `Content`.
   - Has a method `SaveState()` that returns a `TextEditorMemento`.
   - Has a method `RestoreState()` that restores a `TextEditorMemento`.
3. **Create a `HistoryManager` class** that:
   - Manages saved states of the text.
   - Provides functionality to **save** and **undo** text states.
4. **Develop a `TextEditorController`** that:
   - Handles the interactions for **saving** and **undoing** changes.
5. **Implement a view (`Index.cshtml`)** that:
   - Displays a **textarea** for entering text.
   - Provides buttons to **Save** and **Undo** text changes.
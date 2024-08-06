# Features and Description
  - The application allows users to manage their to-do list by adding, saving, toggling the status, and deleting to-do items.

# Languages Used
  -html,CSS,javaScript

# step-by-step explanation

  1. **Loading the Application:**
     
     - The application retrieves existing to-do items from 'localStorage' using the 'getTodoListFromLocalStorage()' function.
     - If there are no items saved, an empty list is returned.
     - The retrieved to-do items are stored in the 'todoList' array, and 'todosCount' is set to the number of to-do items.
       
  2. **Displaying Existing To-dos:**
     
     - The application loops through the todoList array and calls 'createAndAppendTodo(todo)' for each to-do item, which adds them to the DOM.
       
  3. **Adding a New To-do:**
     
     - The user enters a new to-do item in the input field with the id todoUserInput.
     - When the user clicks the "Add Todo" button, the 'onAddTodo()' function is called.
     - If the input field is empty, an alert prompts the user to enter valid text.
     - If valid text is entered, a new to-do object is created with a unique identifier, the entered text, and a isChecked status set to false.
     - The new to-do object is added to the todoList array, and the 'createAndAppendTodo()' function is called to add it to the DOM.
     - The input field is then cleared.
       
  4. **Saving To-dos:**
     
     - When the user clicks the "Save Todo" button, the 'saveTodoButton.onclick' event handler saves the 'todoList' array to 'localStorage'.
       
  5. **Toggling To-do Status:**
      
     - When the user clicks a checkbox next to a to-do item, the 'onTodoStatusChange(checkboxId, labelId, todoId)' function is called.
     - The function toggles the checked class on the label, updating the visual status of the to-do.
     - It also updates the isChecked property of the corresponding to-do object in the todoList array.
      
  6. **Deleting a to-do**
     
     - When the user clicks the delete icon next to a to-do item, the 'onDeleteTodo(todoId)' function is called.
     - The function removes the to-do item from the DOM.
     - It also removes the corresponding to-do object from the todoList array.    
       
  13. ** Creating and Appending To-dos: **

      - The 'createAndAppendTodo(todo)' function is responsible for creating the necessary HTML elements for a to-do item and appending them to the DOM.
      - It creates a li element for the to-do item, including a checkbox, a label, and a delete icon.
      - The checkbox's click event is linked to the 'onTodoStatusChange' function, and the delete icon's click event is linked to the 'onDeleteTodo' function.

By following these steps, the application allows users to manage their to-do list by adding, saving, toggling the status, and deleting to-do items.



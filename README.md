# User-Interface-Specification
User interface specification document  for the user management

## Requirements

-User interface to perform the following actions:

  -View a list of existing users.
  -Hide disabled users.
  -Add a new user.
  -Edit new user details.
  -Save new user.

## UI Components
  
  **User List**
    - Display a table listing all existing users.
    - Each row should display the user's username, email, and enabled status.
    - Clicking on a user's row should highlight it.
  **New User Form**
     - Display a form to add a new user.
     - Include input fields for the user's username, display name, phone, email, user roles, and enabled status.
     - Include a "Save" button to create the user.
  **Hide Disabled User Checkbox**
     - Include a checkbox labeled "Hide Disabled Users" above the User List.
     - When the checkbox is checked, hide the rows of users with the "enabled" status set to disabled.
     - When the checkbox is unchecked, show all users in the User List.

## Page Behavior

- When the User Management screen is loaded:
  - Retrieve the list of existing users from the backend server.
  - Display the User List component with the retrieved user data.
  - The New User Form should be initially hidden.

- What to show to the user at the beginning:
  - Display the User List component with the existing users' data.
  - Show the New User button to add a new user.
  - Show the Hide Disabled User Checkbox to allow hiding disabled users.

- Clicking the "New User" button:
  - Show the New User Form component.
  - Clear all input fields in the form.

- Clicking the "Save User" button in the New User Form :
  - Validate the input fields for completeness and correctness.
  - If valid, send a request to the backend server to create or update the user.
  - Display a success message and refresh the User List.
  - Hide the New User Form.

- Checking the "Hide Disabled Users" checkbox:
  - Hide the rows of users with the "enabled" status set to disabled.


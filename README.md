#EXPLANATION:
Creating a detailed mind map for your C program will help visualize its structure and flow. Below is a step-by-step breakdown of the program's components and their relationships:

*Main Function (`main`)*
- Initialize variables: `name`, `id`, `ch`, `username`, `password`.
- Clear the screen (`system("CLS")`).
- Set console text color to light gray on white (`system("color 8F")`).
- Call the `heading` function to display the program's welcome message.
- Prompt the user to choose between admin and user login (`printf` and `scanf`).
- Clear the screen again (`system("CLS")`).
- Use a `switch` statement based on the user's choice (`ch`).

*Admin Login (`case 1`)*
- Clear the screen again (`system("CLS")`).
- Call the `heading` function.
- Prompt the admin to enter their username and password (`printf` and `scanf`).
- Check if the username is "admin" and the password is "cyber123."
  - If correct, clear the screen and call `main_heading`, then display a welcome message and call the `menu` function.
  - If incorrect, display an error message.

*User Login (`case 2`)*
- Clear the screen again (`system("CLS")`).
- Call the `heading` function.
- Prompt the user to choose between login and sign-up (`printf` and `scanf`).
- Use a nested `switch` statement based on the user's choice (`cho`).
  - If login is chosen (`case 1`):
    - Clear the screen.
    - Call `main_heading`.
    - Call the `login_user` function.
  - If sign-up is chosen (`case 2`):
    - Clear the screen.
    - Call `main_heading`.
    - Call the `user_login` function.
  - Display an error message for invalid choices (`default`).

*Utility Functions (`heading` and `main_heading`)*
- Display formatted program headers using `printf`.

*Admin Menu (`menu`)*
- Display a menu with options:
  - Insert Record
  - Display Record
  - Search Record
  - Delete Record
  - Exit
- Prompt the admin to choose an option (`printf` and `scanf`).
- Use a `switch` statement based on the chosen option.
  - Call corresponding functions (`insert`, `display`, `search`, `delete`, or `exit`) based on the option.

*User Menu (`user_menu`)*
- Display a menu with options:
  - View Your Record
  - Exit
- Prompt the user to choose an option (`printf` and `scanf`).
- Use a `switch` statement based on the chosen option.
  - Call corresponding functions (`search` or `exit`) based on the option.

*Insert Record (`insert`)*
- Get the current time using `time` and `localtime`.
- Open a file in append mode (`fopen`).
- Use a loop to repeatedly insert user data:
  - Prompt for User_ID and Name.
  - Write data to the file.
  - Calculate and display arrival time using `arrival_time`.
  - Ask if the admin wants to add another record.

*Display Record (`display`)*
- Open the file for reading (`fopen`).
- Display user details, including ID, Name, Date, Time, and Duration.
- Calculate and display the duration.
- Check for malicious activity (duration > 300 minutes).
- Wait for user input to continue (`getchar`).

*Search Record (`search`)*
- Open the file for reading.
- Prompt for a user ID to fetch information.
- Display the user's information if found.
- Check for malicious activity (duration > 300 minutes).
- Display a "Record not found" message if the record is not found.

*Delete Record (`delete`)*
- Open the file for reading.
- Prompt for a user ID to delete.
- Create a new file to store records without the specified ID.
- Copy records to the new file without that ID.
- Delete the original file and rename the new file.
- Display a "Record Deleted Successfully" message.
- Display updated records.
- Wait for user input to continue (`getchar`).

*Arrival Time (`arrival_time`)*
- Get the current time and date using `time`, `localtime`, and `strftime`.
- Display the arrival time and date.

*User Login (`user_login`)*
- Prompt for a username and password.
- Store the user's data in a file.

*Login User (`login_user`)*
- Prompt for a username and password.
- Check if the provided credentials match those stored in the file.
- Display a welcome message for successful login.
- Display an error message for incorrect credentials.

This detailed mind map provides an organized overview of the program's structure and functionality.


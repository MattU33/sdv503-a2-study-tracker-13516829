Study Tracker System

A command-line terminal application built to log, validate, and aggregate historical study sessions.


Technical Setup & Installation

Before running the application, ensure you have the proper runtime environment and dependencies installed:

1. **Install Node.js:** Make sure Node.js is installed on your local machine.
2. **Install Dependencies:** Open your terminal and install the required user-input tracking library by running:
   ```bash
   npm install readline-sync


   Operation Instructions
These are the operations you should perform to launch and operate on the application interface.

Step 1: Make sure that the terminal window is launched and in the project folder root directory.

Step 2: Run the application through the command node SDV503-A2.js.

Step 3: Select any of the available menu options (1-3).

Step 4: Select option 1 from the terminal window and press Enter.

Step 4a: Enter the study topic name and the time spent studying in minutes when prompted.

Step 4b: Inputs are checked to see whether they satisfy the constraints. For example, if topic name input field has no characters or is empty, or the duration is a decimal, negative number, or zero, the entry will not be allowed in the system.

Step 4c: If there is room for a new entry in the memory database, then the entry will be created, and the terminal will display a confirmation message.

Step 5: Type in 2 in the terminal to get the list of existing Historical Study Sessions.

Step 5a: In case there are no existing study sessions in the system, then the message is displayed stating that no study sessions have been found yet.

Step 5b: In case the data exists, the system will display the current session list consisting of the number of the row, topic names, and explicitly stated amount of minutes spent.

Step 5c: The system will automatically make an aggregation check and display the total sum of your time spent as TOTAL TIME ELAPSED.

Step 6: Type in 3 in the terminal to close the system.

Step 6a: After the interface stream is shut down, you will get back to your usual terminal environment.
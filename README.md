# flightDB
Flight Service application
The objective of the project is to practice working with process creation, signals, and interprocess communication using pipes. The application is designed to be an interactive multi-process application, divided into two processes. The first process interacts with the user, while the second process performs operations on a database (DB).

The program is divided into two processes:
1. Main Process: This process creates a child process upon initialization and handles user input and output. When the user chooses options 1-5, the request is passed from the main process to the child process, and the result data is received from the child process.
2. Child Process: This process receives operation codes (op-codes) from the main process, performs the required operation, and returns the data.

Technologies Used:
1. CMake: The project is built using CMake, a cross-platform build system.
2. Shared Object (Utility): The project utilizes shared objects for modularization and code reuse.
3. libzip: The project links with the libzip library, which is used for zipping and unzipping DB files.
4. Pipes: Interprocess communication is achieved using pipes to pass requests and data between the main process and the child process.
5. Bash: Bash scripting is used to update the existing airports in the DB with recent data by running a BASH script.
6. cURL: The project uses cURL, a command-line tool, to fetch data from an API for processing in the application.

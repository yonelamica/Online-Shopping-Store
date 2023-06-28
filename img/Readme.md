PoisePMSProgram
This is a Java program that interacts with a MySQL database for managing projects and associated people in a construction project management system called PoisePMS.

Prerequisites
Before running the program, ensure that you have the following prerequisites:

Java Development Kit (JDK) installed on your system
MySQL database server installed and running.
MySQL Connector/J library added to your project dependencies.
Configuration
The program connects to the MySQL database using the following configuration:

Database URL: jdbc:mysql://localhost:3306/poisepms
Username: `your_username`
Password: `your_password`
You may need to modify these values in the DB_URL, DB_USERNAME, and DB_PASSWORD constants if your MySQL server is configured differently.

Functionality
The program provides the following functionality:

Display all projects and associated people
Add a new project
Update an existing project
Delete a project and associated people
Finalize a project
Find all projects that still need to be completed
Find all projects that are past the due date
Find and select a project by project number or name
Exit the program
Usage
To use the program, follow these steps:

Compile the Java code using the Java compiler (javac):


javac PoisePMSProgram.java
Run the compiled program using the Java Virtual Machine (java):


java PoisePMSProgram
The program will display a menu with options. Enter the number corresponding to the desired option and press Enter to execute it.

Follow the prompts and provide the required information as per the selected option.

Repeat steps 3 and 4 until you choose to exit the program.

To close the program and release the database connection, select option 9 from the menu.

Closing the Connection
After using the program, it is recommended to close the database connection to release system resources. To do this, call the closeConnection() method of the PoisePMSProgram class. This method will attempt to close the connection gracefully.


program.closeConnection();
Note that this method is not called automatically in the program but should be invoked explicitly when you are finished using the program.

Disclaimer
This program assumes that the necessary database schema and tables (Projects and Employees) are already created in the MySQL database. The program uses raw SQL queries for simplicity and assumes the existence of the required database objects. Make sure your database is set up accordingly before using the program.

License
This code is released under the MIT License. Feel free to modify and use it as per your needs.
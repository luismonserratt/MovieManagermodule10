======================================================
             Movie Manager - Java + MySQL + Swing
======================================================

Author: Luis Augusto Monserratt Alvarado  
Date: July 2025  
Project: Module 10 - Movie Manager with Database Integration  

------------------------------------------------------
Description:
------------------------------------------------------
This application is a simple Java Swing GUI program for managing a movie database using MySQL.  
It allows the user to:

- View all movies in the database
- Add a new movie
- Update an existing movie
- Delete a movie
- Calculate and display the average duration of all movies
- Test MySQL connection

------------------------------------------------------
Project Structure:
------------------------------------------------------
src/com/luismonserratt/moviemanager/
├── Movie.java                  → Represents a movie object  
├── MovieDAO.java              → Handles all database operations (CRUD + AVG)  
├── DatabaseManager.java       → Manages MySQL connection settings  
├── MovieManagerGUI.java       → Main GUI class (start here)  
├── MySQLConnectionTest.java   → Optional class to test DB connection  

sql/
├── movie_manager.sql          → SQL script to create the database, table, and insert sample data

lib/
├── mysql-connector-j-8.x.x.jar → MySQL JDBC driver (required)

------------------------------------------------------
How to Run:
------------------------------------------------------
1. Make sure MySQL is installed and running on your machine.

2. Open a MySQL terminal and execute the SQL script:
   > USE movie_manager;  
   > Run the contents of `movie_manager.sql` to create the table and insert sample data.

3. Open the project in IntelliJ IDEA or your preferred Java IDE.

4. Add the MySQL connector JAR file to your project's libraries:
   - Go to Project Structure → Modules → Dependencies
   - Click `+` → JARs or directories → Select the `mysql-connector-j-8.x.x.jar`

5. Open and run `MovieManagerGUI.java`.

------------------------------------------------------
MySQL Configuration:
------------------------------------------------------
Default configuration is located in `DatabaseManager.java`:

URL: `jdbc:mysql://localhost:3306/movie_manager`  
User: `root`  
Password: `Luis123!`  

You can modify these credentials if needed.

------------------------------------------------------
Note:
------------------------------------------------------
- Make sure to have the MySQL JDBC driver in your classpath.
- This project is designed to demonstrate basic database interaction with Java and Swing.

------------------------------------------------------
Enjoy using the Movie Manager!
======================================================

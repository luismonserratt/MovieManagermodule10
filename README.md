# 🎬 Movie Manager (Java + MySQL)

A desktop-based Movie Manager application built using **Java Swing** and **MySQL**. This app allows users to manage a collection of movies with features like adding, updating, deleting, and viewing movies, as well as calculating the average duration.

---

## 📦 Features

- Connect to a local MySQL database
- View all movies in the database
- Add new movies
- Update existing movie details
- Delete movies by title
- Display average movie duration

---

## 🛠️ Technologies Used

- Java 17+
- Java Swing (GUI)
- MySQL 8.0+
- JDBC (MySQL Connector/J)
- IntelliJ IDEA

---

## 🧱 Database Setup

1. **Create the Database and Table**

Login to MySQL and execute:

```sql
CREATE DATABASE IF NOT EXISTS movie_manager;
USE movie_manager;

CREATE TABLE IF NOT EXISTS movies (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(100) NOT NULL,
    genre VARCHAR(50),
    year INT,
    rating DOUBLE,
    duration INT,
    watched BOOLEAN
);

-- Insert sample data
INSERT INTO movies (title, genre, year, rating, duration, watched) VALUES
('Inception', 'Sci-Fi', 2010, 8.8, 148, true),
('Titanic', 'Romance', 1997, 7.8, 195, true),
('Interstellar', 'Sci-Fi', 2014, 8.6, 169, true),
('Shrek', 'Comedy', 2001, 7.9, 90, true),
('The Godfather', 'Crime', 1972, 9.2, 175, true),
('Toy Story', 'Animation', 1995, 8.3, 81, true),
('Coco', 'Animation', 2017, 8.4, 105, true),
('Joker', 'Drama', 2019, 8.5, 122, true),
('Iron Man', 'Action', 2008, 7.9, 126, true),
('Frozen', 'Animation', 2013, 7.4, 102, true);

Update Connection Info

Make sure the DatabaseManager.java file contains your correct database settings:

private static final String URL = "jdbc:mysql://localhost:3306/movie_manager";
private static final String USER = "root";
private static final String PASSWORD = "your_password";

How to Run
Open the project in IntelliJ IDEA.

Make sure MySQL is running.

Install mysql-connector-j if it's not already included (check your lib or Maven dependencies).

Run MovieManagerGUI.java as a Java application.

Project Structure:

src/
└── com.luismonserratt.moviemanager/
    ├── Movie.java
    ├── MovieDAO.java
    ├── MovieManagerGUI.java
    ├── DatabaseManager.java
    └── MySQLConnectionTest.java

Author
Luis Augusto Monserratt Alvarado
GitHub: @luismonserratt

# Book Library System (PHP + MySQL)

This is a simple Book Library System built using PHP and MySQL. It allows users to add and search books using a basic web interface.

---

# Features

- Add a new book
- Search books by title or author
- Simple HTML form interface
- MySQL database integration

---

# Requirements

- XAMPP or any local server (Apache + MySQL)
- PHP 7 or higher
- MySQL / phpMyAdmin
- Web browser

---

# Installation Guide

## 1. Clone the repository

git clone https://github.com/kuyahos/books.git

---

## 2. Move project to server directory

If using XAMPP, move the folder to:

htdocs/books

---

## 3. Start server

Open XAMPP and start:

- Apache
- MySQL

---

## 4. Create the database

Open phpMyAdmin and run the following SQL commands:

CREATE DATABASE library_db;

USE library_db;

CREATE TABLE books (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    author VARCHAR(255) NOT NULL,
    year INT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

---

## 5. Configure database connection

Open db.php and make sure the settings match your local server:

$host = "localhost";
$user = "root";
$password = "";
$database = "library_db";

---

## 6. Run the project

Open your browser and go to:

http://localhost/books/index.php

---

# Project Structure

books/
│
├── db.php
├── index.php
├── add.php
├── search.php
├── style.css
└── README.md

---

# How it works

## Add Book
- Fill out the form in the homepage
- Click "Add Book"
- Data will be stored in MySQL database

## Search Book
- Enter a keyword (title or author)
- Click "Search"
- Matching results will be displayed

---

# Notes

- This is a basic PHP project for learning purposes
- No authentication system included
- No prepared statements (not yet secure for production use)

---

# Future Improvements

- Add edit and delete features
- Add login system
- Use prepared statements for security
- Improve UI design
- Add book cover image upload

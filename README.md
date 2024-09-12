## SQL Files

Here is the SQL file used in this project:

- [LibraryDB.sql](path/to/LibraryDB.sql)


## SQL Schema Example

```sql
-- Content of LibraryDB.sql

CREATE TABLE authors (
    author_id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL
);

CREATE TABLE books (
    book_id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    author_id INT,
    publication_year INT,
    genre VARCHAR(50),
    available_copies INT,
    FOREIGN KEY (author_id) REFERENCES authors(author_id)
);

CREATE TABLE users (
    user_id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    email VARCHAR(100) NOT NULL
);

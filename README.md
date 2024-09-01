# Book_Curd

A simple RESTful API built with Flask and SQLite3 for managing a collection of books.

## Installation

To set up and run this project, ensure you have the following installed:

- **Python**
- **Flask API**
- **SQLite3**

## API Endpoints

### 1. POST /books/
Create a new book in the database.

- **Method**: `POST`
- **URL**: `/books/`
- **Content-Type**: `application/json`
- **Body**: (JSON)
    ```json
    {
      "title": "The Great Gatsby",
      "author": "F. Scott Fitzgerald",
      "published_date": "1925-04-10",
      "isbn": "9780743273565",
      "page_count": 180,
      "cover": "http://example.com/gatsby.jpg",
      "language": "English"
    }
    ```

### 2. GET /books/{id}
Retrieve details of a specific book by its ID.

- **Method**: `GET`
- **URL**: `/books/{id}`

### 3. GET /books/
Retrieve books with optional filters for author, published date, and language.

- **Method**: `GET`
- **URL**: `/books?author={author}&published_date={published_date}&language={language}`
- **Example**: `/books?author=F. Scott Fitzgerald&language=English`

### 4. PUT /books/{id}
Update an existing book by its ID.

- **Method**: `PUT`
- **URL**: `/books/{id}`
- **Content-Type**: `application/json`
- **Body**: (JSON) Partial or full update
    ```json
    {
      "title": "The Great Gatsby (Updated)",
      "page_count": 200
    }
    ```

### 5. DELETE /books/{id}
Delete a book by its ID.

- **Method**: `DELETE`
- **URL**: `/books/{id}`

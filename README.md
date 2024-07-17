# Go Bookstore Backend

This is a backend API for a bookstore, built with Go, Gorilla Mux for routing, and GORM for MySQL database interaction.

## Features

- Create a new book
- Retrieve all books
- Retrieve a book by its ID
- Update a book by its ID
- Delete a book by its ID

## Prerequisites

- Go 1.16+
- MySQL
- Git

## Installation

1. **Clone the repository:**
   ```sh
   git clone https://github.com/your-username/go-bookstore-backend.git
   cd go-bookstore-backend
   ```

2. **Install dependencies:**
   ```sh
   go mod tidy
   ```

3. **Set up MySQL database:**
   - Create a database in MySQL.
   - Update the database connection details in your application configuration (e.g., `config/config.go`).

4. **Run the application:**
   ```sh
   go run main.go
   ```

## API Routes

The following routes are available in the API:

- **Create a new book**
  - **URL:** `/book/`
  - **Method:** `POST`
  - **Description:** Creates a new book in the bookstore.
  
- **Retrieve all books**
  - **URL:** `/book/`
  - **Method:** `GET`
  - **Description:** Retrieves all books in the bookstore.

- **Retrieve a book by ID**
  - **URL:** `/book/{bookId}`
  - **Method:** `GET`
  - **Description:** Retrieves a book by its ID.

- **Update a book by ID**
  - **URL:** `/book/{bookId}`
  - **Method:** `PUT`
  - **Description:** Updates a book by its ID.

- **Delete a book by ID**
  - **URL:** `/book/{bookId}`
  - **Method:** `DELETE`
  - **Description:** Deletes a book by its ID.

## Example Usage

### Creating a new book

```sh
curl -X POST http://localhost:8080/book/ -d '{
  "Title": "The Catcher in the Rye",
  "Author": "J.D. Salinger",
  "Publisher": "Little, Brown and Company"
}'
```

### Getting all books

```sh
curl http://localhost:8080/book/
```

### Getting a book by ID

```sh
curl http://localhost:8080/book/1
```

### Updating a book

```sh
curl -X PUT http://localhost:8080/book/1 -d '{
  "Title": "The Catcher in the Rye",
  "Author": "Jerome David Salinger",
  "Publisher": "Little, Brown and Company"
}'
```

### Deleting a book

```sh
curl -X DELETE http://localhost:8080/book/1
```

## Dependencies

- [Gorilla Mux](https://github.com/gorilla/mux): A powerful URL router and dispatcher for Golang.
- [GORM](https://gorm.io/): The fantastic ORM library for Golang.
- [MySQL](https://www.mysql.com/): The world's most popular open-source database.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Author

- [Shabaj Ansari](https://github.com/SHabaj.dev)

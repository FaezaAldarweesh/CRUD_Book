# CRUD Book Management System

This project is a simple CRUD **Book Management System** built with **Laravel**, which implements basic CRUD operations (Create, Read, Update, Delete) for managing a collection of books. The system allows users to add, update, view, and delete books with features like soft deletion and filtering based on the `is_active` status of books.

## Features

- **Create Books**: Add new books with title, author, and publication date.
- **Read Books**: View a list of all books in the system with filtering options.
- **Update Books**: Edit book details including title, author, and publication date.
- **Delete Books**: Soft delete functionality is enabled, allowing for temporary removal of books.
- **Filter Books**: Filter books based on their `is_active` status to show only available or unavailable books.
  
## Installation

1. Clone the repository: git clone https://github.com/FaezaAldarweesh/CRUD_Book.git
2. composer install
3. cp .env.example .env
4. php artisan key:generate
5. php artisan migrate
6. php artisan serve

## API Endpoints
1. Get All Books : POST /api/books (with ability to filter on is_active (optional): Set to 1 to retrieve only available books, or 0 to retrieve unavailable books. Endpoint:  GET /api/books?is_active=1)
2. Create a Book : POST /api/books
3. Update a Book : PUT /api/books/{id}
4. Delete a Book : DELETE /api/books/{id} (soft delete)
5. GEt All Trashed Books : /api/all_trashed_book
6. Restore Book from soft delete : /api/restore_book/{id}
7. Force delete book from after trashed it : /api/forceDelete_book/{id}

## Linke PostMan Documentation : https://documenter.getpostman.com/view/34467473/2sAXqtb27t

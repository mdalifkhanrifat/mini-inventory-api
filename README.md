
# Mini Inventory Management API (Laravel)

This is a basic inventory management API built with **Laravel** and **Sanctum Authentication**. It allows you to manage categories and products, with the ability to create, read, update, and delete resources.

## Features

- **Product Management**
  - Create, read, update, and delete products
  - Each product has a `name`, `price`, `quantity`, and `category_id`
  
- **Category Management**
  - Create and list categories
  - Products are associated with categories
  
- **Authentication**
  - User registration and login using **Sanctum**
  - Bearer token authentication for protected routes

## Tech Stack

- **Backend:** Laravel 12
- **Authentication:** Sanctum (API Tokens)
- **Database:** MySQL
- **Frontend:** N/A (API only)
- **Hosting (Optional):** N/A (Railway/Render)

## Installation

### Clone the Repository
```bash
git clone https://github.com/mdalifkhanrifat/mini-inventory-api.git
cd mini-inventory-api
```

### Install Dependencies
```bash
composer install
```

### Set up Environment
Create .env file:
```bash
cp .env.example .env
```

Generate application key:
```bash
php artisan key:generate
```

### Database Configuration
Configure the .env file with your database connection settings:

```plaintext
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database_name
DB_USERNAME=your_database_user
DB_PASSWORD=your_database_password
```

### Migrate Database
Run the database migrations:
```bash
php artisan migrate
```

### Run the Server
Now you can run the Laravel development server:
```bash
php artisan serve
```
The API should now be running at `http://localhost:8000`.

## API Documentation

### Authentication Routes
- **POST /api/register**: Register a new user.
- **POST /api/login**: Log in a user and return a Bearer token.
- **POST /api/logout**: Logs out the authenticated user. Requires Bearer token.

### Category Routes
- **GET /api/categories**: Get all categories.
- **POST /api/categories**: Create a new category.
- **PUT /api/categories/{id}**: Update an existing category.
- **DELETE /api/categories/{id}**: Delete a category.

### Product Routes
- **GET /api/products**: Get all products.
- **POST /api/products**: Create a new product.
- **GET /api/products/{id}**: Get a specific product by ID.
- **PUT /api/products/{id}**: Update a product.
- **DELETE /api/products/{id}**: Delete a product.

### Filter Products by Category
- **GET /api/categories/{id}/products**: Get all products in a specific category.

## Testing the API
1. **Register a User** using POST `/api/register`.
2. **Login the User** using POST `/api/login` to get the Bearer token.
3. Use the Bearer token in the **Authorization header** to test protected routes:
```plaintext
Authorization: Bearer <your_token>
```
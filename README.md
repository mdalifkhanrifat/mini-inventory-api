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
- **Hosting (Optional):** Railway/Render

## Installation

### Clone the Repository
```bash
git clone https://github.com/mdalifkhanrifat/mini-inventory-api.git
cd mini-inventory-api

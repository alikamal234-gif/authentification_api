# Authentication API

A RESTful API built with **Laravel** that provides secure user authentication and profile management using token-based authentication.

This API allows users to:

- Register a new account
- Login and receive an authentication token
- Logout securely
- View their profile
- Update profile information
- Change password
- Delete their account

---

# Features

- Laravel REST API
- Token-based authentication
- User profile management
- Password change functionality
- Secure logout
- Account deletion
- Postman collection for testing

---

# Tech Stack

- Laravel 12
- PHP 8+
- MySQL
- JWT / Token Authentication
- Postman

---

# Installation

## 1 Clone the repository

git clone https://github.com/yourusername/authentication-api.git
cd authentication-api
2 Install dependencies
composer install
3 Create environment file
cp .env.example .env
4 Generate application key
php artisan key:generate
5 Configure database

Update .env

DB_DATABASE=auth_api
DB_USERNAME=root
DB_PASSWORD=
6 Run migrations
php artisan migrate
7 Start server
php artisan serve

API will run on

http://localhost:8000
API Base URL
http://localhost:8000/api
Authentication

Protected endpoints require a Bearer Token

Example header

Authorization: Bearer {token}
API Endpoints
Auth
Method	Endpoint	Description
POST	/register	Register new user
POST	/login	Authenticate user
POST	/logout	Logout user
Profile
Method	Endpoint	Description
GET	/profile	Get authenticated user profile
PUT	/updateprofile	Update user profile
PATCH	/changepassword	Change user password
DELETE	/deletecomte	Delete user account
Example Requests
Login
POST /api/login

Body

{
  "email": "user@email.com",
  "password": "password"
}

Response

{
  "message": "Login successful",
  "token": "your_access_token"
}
Change Password
PATCH /api/changepassword

Body

{
  "password": "currentpassword",
  "new_password": "newpassword",
  "confirme_new_password": "newpassword"
}
Postman

Import the Postman collection and set the environment variable

base_url = http://localhost:8000/api

Then login to get the token.

Project Structure
app
 ├── Http
 │   ├── Controllers
 │   │   ├── AuthController.php
 │   │   └── ProfileController.php
 ├── Models
 │   └── User.php
routes
 └── api.php
Author

.

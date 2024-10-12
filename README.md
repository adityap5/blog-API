# Blogging Platform API

This is a simple RESTful API for a blogging platform, built using Express.js for Node.js, MongoDB for the database, and token-based authentication for secure access.

## Features

- User registration and authentication
- Create, read, update, and delete (CRUD) operations for blog posts
- Token-based authentication to secure API endpoints

## Technologies Used

- **Framework:** Express.js
- **Database:** MongoDB
- **Authentication:** JWT (JSON Web Token)

## Getting Started

### Prerequisites

- Node.js installed on your machine
- MongoDB installed or access to a MongoDB cloud instance
- Postman or a similar tool for testing API endpoints

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/adityap5/blog-API.git
   cd blogging-platform-api
   
2  **Install dependencies:**

    npm install

3  **Set up environment variables:**
   Create a .env file in the root directory and add the following:

     MONGO_URI=mongodb://localhost:27017/yourdbname
     JWT_SECRET=your_secret_key

4. **Run the server:**

       npm run dev

The server will start on http://localhost:5000.

**API Endpoints**
User Authentication

Register a User
Method: POST
URL: /api/auth/register

Request Body:

     {
    "username": "your_username",
    "password": "your_password"
     }

Login a User
Method: POST
URL: /api/auth/login

Request Body:

    {
    "username": "your_username",
    "password": "your_password"
    }
    
Response:
 
    {
     "token": "your_jwt_token"
    }
    
Blog Posts

Create a New Blog Post
Method: POST
URL: /api/post

Headers:
Authorization: <your_jwt_token>

Request Body:

    {
    "title": "Your Blog Post Title",
    "content": "Your blog post content."
    }
    
Retrieve All Blog Posts
Method: GET
URL: /api/post

Retrieve a Single Blog Post by ID
Method: GET
URL: /api/post/:id

Update an Existing Blog Post
Method: PUT
URL: /api/post/:id

Headers:
Authorization: <your_jwt_token>

Request Body:

    {
    "title": "Updated Blog Post Title",
    "content": "Updated blog post content."
    }
    
Delete a Blog Post
Method: DELETE
URL: /api/post/:id

Headers:
Authorization: <your_jwt_token>


Contact
If you have any questions or feedback, feel free to reach out.

Author: Aditya Pippal
Email: aditya29pippal@gmail.com 
GitHub: adityap5




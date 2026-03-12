# Node.js GraphQL Backend

A **Node.js backend API** built with **Express, GraphQL, MongoDB, and JWT authentication**.
This project demonstrates how to build a backend with **authentication, file uploads, and GraphQL APIs**.

---

# Features

* GraphQL API using `express-graphql`
* JWT-based authentication
* MongoDB database with Mongoose
* File uploads using Multer
* Input validation with `express-validator`
* Authorization middleware
* REST endpoints for authentication
* Modular project structure

---

# Tech Stack

* **Node.js**
* **Express.js**
* **GraphQL**
* **MongoDB**
* **Mongoose**
* **JWT Authentication**
* **Multer (File Uploads)**
* **Express Validator**

---

# Project Structure

```
backend
│
├── app.js                # Main application entry point
├── package.json
│
├── controllers           # Business logic
│   ├── auth.js
│   └── feed.js
│
├── graphql               # GraphQL setup
│   ├── schema.js
│   └── resolver.js
│
├── middleware
│   └── is-auth.js        # Authentication middleware
│
├── models                # MongoDB models
│   ├── user.js
│   └── post.js
│
├── routes                # REST routes
│   ├── auth.js
│   └── feed.js
│
├── images                # Uploaded images
│
└── .gitignore
```

---

# Installation

Clone the repository

```bash
git clone https://github.com/Aditya-droid-byte/Basic_social_media_clone.git
cd backend
```

Install dependencies

```bash
npm install
```

---

# Running the Application

Start the development server

```bash
npm start
```

Server will run on:

```
http://localhost:8080
```

---

# GraphQL Endpoint

```
http://localhost:8080/graphql
```

You can test GraphQL queries using:

* GraphQL Playground
* Postman
* Apollo Client
* GraphiQL

---

# Authentication

Authentication uses **JWT tokens**.

Workflow:

1. User signs up
2. User logs in
3. Server returns JWT token
4. Client sends token in request headers

Example header:

```
Authorization: Bearer <token>
```

---

# File Uploads

File uploads are handled using **Multer**.

Uploaded files are stored in:

```
/images
```

The API supports uploading images when creating or updating posts.

---

# Example GraphQL Queries

### Fetch Posts

```graphql
query {
  posts {
    _id
    title
    content
  }
}
```

---

### Create Post

```graphql
mutation {
  createPost(postInput: {
    title: "My Post"
    content: "This is a sample post"
  }) {
    _id
    title
    content
  }
}
```

---

# Example Auth REST API

### Signup

```
POST /auth/signup
```

### Login

```
POST /auth/login
```

Response returns a **JWT token**.

---

# Environment Variables (Recommended)

Create a `.env` file:

```
MONGODB_URI=your_mongodb_connection
JWT_SECRET=your_secret_key
PORT=8080
```

---

# Dependencies

Main dependencies used in the project:

* express
* graphql
* express-graphql
* mongoose
* jsonwebtoken
* bcryptjs
* multer
* express-validator
* body-parser

---

# Development

For development the project uses:

```
nodemon
```

Run with:

```bash
npm start
```

---

# License

This project is licensed under the **ISC License**.

---

# Author

Aditya Srivastava

---

# Future Improvements

Possible improvements:

* Add **GraphQL subscriptions**
* Add **Redis caching**
* Implement **pagination**
* Add **Docker support**
* Improve **error handling**

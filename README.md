# Node.js GraphQL Backend Demonstration Project

This project is a **backend-focused full stack demo** designed to showcase **Node.js backend development skills**.

The primary goal of this repository is to demonstrate the implementation of a **production-style backend architecture using Node.js, Express, GraphQL, MongoDB, and JWT authentication**.

A minimal **React frontend is included only as a testing interface** to interact with the backend APIs. The frontend is **not the focus of this project** and is intentionally kept simple.

---

# Project Goal

The objective of this project is to demonstrate backend engineering concepts such as:

* Designing **GraphQL APIs**
* Implementing **authentication and authorization**
* Structuring a **Node.js backend application**
* Working with **MongoDB using Mongoose**
* Handling **file uploads**
* Implementing **middleware for security and request validation**
* Building **modular and scalable backend architecture**

The React frontend is only used to **consume the APIs and verify backend functionality**.

---

# Backend Features (Core Focus)

### Authentication System

* User signup and login
* JWT-based authentication
* Authorization middleware
* Secure route protection

### GraphQL API

* Query posts and users
* Create posts
* Edit posts
* Delete posts
* Fetch individual posts

### File Uploads

* Image uploads using **Multer**
* Image storage on the server
* Image preview before upload

### Data Layer

* MongoDB database
* Mongoose schema models
* Relationships between users and posts

### Middleware

* Authentication middleware
* Input validation using **express-validator**
* Error handling

---

# Tech Stack

## Backend (Primary Focus)

* **Node.js**
* **Express.js**
* **GraphQL**
* **MongoDB**
* **Mongoose**
* **JWT Authentication**
* **Multer**
* **Express Validator**

## Frontend (Support Only)

* **React.js**
* Used only to test the backend APIs

---

# Architecture Overview

```
React Client (Testing Interface)
           │
           │ GraphQL Requests
           ▼
Node.js + Express Backend
           │
           │ GraphQL Resolvers
           ▼
MongoDB Database
```

The backend exposes a **GraphQL API** that handles authentication, post management, and file uploads.

---

# Project Structure

```
project
│
├── backend
│   ├── app.js
│   │
│   ├── controllers
│   │   ├── auth.js
│   │   └── feed.js
│   │
│   ├── graphql
│   │   ├── schema.js
│   │   └── resolver.js
│   │
│   ├── middleware
│   │   └── is-auth.js
│   │
│   ├── models
│   │   ├── user.js
│   │   └── post.js
│   │
│   ├── routes
│   │   ├── auth.js
│   │   └── feed.js
│   │
│   └── images
│
└── frontend
    ├── public
    └── src
```

---

# Running the Project

## 1. Start Backend

```
cd backend
npm install
npm start
```

Backend runs on:

```
http://localhost:8080
```

GraphQL endpoint:

```
http://localhost:8080/graphql
```

---

## 2. Start Frontend (Optional)

The frontend is **optional** and exists only to interact with the backend.

```
cd frontend
npm install
npm start
```

Frontend runs on:

```
http://localhost:3000
```

---

# Environment Variables

Create a `.env` file in the backend folder.

```
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
PORT=8080
```

---

# Authentication Flow

1. User signs up.
2. User logs in.
3. Backend generates a **JWT token**.
4. Client includes the token in request headers.

Example header:

```
Authorization: Bearer <token>
```

---

# Example GraphQL Query

Fetch posts:

```graphql
query {
  posts {
    _id
    title
    content
    creator {
      name
    }
  }
}
```

---

# Example GraphQL Mutation

Create a post:

```graphql
mutation {
  createPost(postInput: {
    title: "Backend Demo"
    content: "This post was created through GraphQL."
  }) {
    _id
    title
    content
  }
}
```

---

# Learning Objectives Demonstrated

This project demonstrates practical backend skills including:

* Designing **GraphQL schemas and resolvers**
* Implementing **JWT authentication**
* Handling **file uploads in Node.js**
* Building **REST + GraphQL hybrid APIs**
* Structuring a **scalable Node.js project**
* Integrating **MongoDB with Mongoose**
* Implementing **backend middleware**

---

# License

ISC License

---

# Author

Aditya Srivastava

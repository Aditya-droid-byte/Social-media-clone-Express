# React GraphQL Frontend

A **React.js frontend application** for a social feed/blog platform.
This application connects to a **Node.js + GraphQL backend** to provide authentication, post creation, image uploads, and feed browsing.

---

# Features

* User Authentication (Signup / Login)
* Create, edit, and delete posts
* Image upload support
* Feed with pagination
* View single post
* Responsive navigation
* Error handling and loading states

---

# Tech Stack

* **React.js**
* **GraphQL API**
* **CSS Modules**
* **Fetch API**
* **JWT Authentication**
* **Reusable UI Components**

---

# Project Structure

```text
frontend
│
├── public
│   ├── index.html
│   ├── favicon.ico
│   └── manifest.json
│
├── src
│   │
│   ├── components
│   │   ├── Backdrop
│   │   ├── Button
│   │   ├── ErrorHandler
│   │   ├── Feed
│   │   ├── Form
│   │   ├── Image
│   │   ├── Layout
│   │   ├── Loader
│   │   ├── Logo
│   │   ├── Modal
│   │   ├── Navigation
│   │   ├── Paginator
│   │   └── Toolbar
│   │
│   ├── pages
│   │   ├── Auth
│   │   │   ├── Login.js
│   │   │   └── Signup.js
│   │   │
│   │   └── Feed
│   │       ├── Feed.js
│   │       └── SinglePost
│   │
│   ├── util
│   │   ├── validators.js
│   │   └── image.js
│   │
│   ├── App.js
│   ├── index.js
│   ├── App.css
│   └── index.css
│
├── package.json
└── .gitignore
```

---

# Installation

Clone the repository:

```bash
git clone https://github.com/Aditya-droid-byte/Basic_social_media_clone.git
cd frontend
```

Install dependencies:

```bash
npm install
```

---

# Running the Application

Start the development server:

```bash
npm start
```

The app will run on:

```
http://localhost:3000
```

---

# Backend Requirement

This frontend expects the **GraphQL backend** to be running at:

```
http://localhost:8080/graphql
```

Make sure the backend server is running before starting the frontend.

---

# Authentication Flow

1. User signs up using the **Signup page**
2. User logs in using the **Login page**
3. Backend returns a **JWT token**
4. Token is stored on the client
5. Authenticated requests include the token in headers

Example header:

```
Authorization: Bearer <token>
```

---

# Feed Features

Users can:

* Create new posts
* Upload images
* Edit posts
* Delete posts
* View a feed of posts
* View individual post details

---

# Image Uploads

Images are uploaded with posts and stored on the backend server.

The frontend handles:

* Image preview
* File validation
* Upload through GraphQL mutation

---

# Example GraphQL Request

Example query to fetch posts:

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

# Development

The project uses:

```
Create React App
```

Common scripts:

Run development server

```
npm start
```

Build production version

```
npm run build
```

Run tests

```
npm test
```

---

# License

This project is licensed under the **ISC License**.

---

# Author

Aditya Srivastava

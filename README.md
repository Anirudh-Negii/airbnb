# 🏠 Airbnb 

> ⚠️ This project is currently **Work In Progress (WIP)**.
> Features, routes, validation behavior, and architecture may change as development continues.

---

## 📌 Overview

This is a **backend-focused Airbnb-style application** built with **Node.js and Express** following an MVC architecture.
It supports user authentication and authorization, session-based login state, image upload handling, and route-driven REST-style operations for homes and favourites.

The project is primarily aimed at learning and implementing **real-world backend development concepts** such as session lifecycle management, protected routing, structured controllers, and scalable project organization.

---

## 🚀 Key Features

*  Authentication with signup / login / logout flow
*  Authorization using protected host routes
*  Session management with cookies (`express-session`)
*  Persistent session storage in MongoDB (`connect-mongodb-session`)
*  Password hashing using `bcryptjs`
*  File upload support for home photos using `multer`
*  Validation and sanitization using `express-validator`
*  CRUD-style operations for homes
*  Favourite management for users
*  Server-side rendering with EJS templates

---

## 🛠️ Tech Stack

* **Runtime:** Node.js
* **Server Framework:** Express.js
* **Database:** MongoDB (Mongoose ODM)
* **Session Store:** MongoDB (`connect-mongodb-session`)
* **Auth & Security:** `bcryptjs`, `express-session`, `express-validator`
* **File Upload:** `multer`
* **Views / Templating:** EJS
* **Styling / Build Tooling:** Tailwind CSS, PostCSS, Autoprefixer
* **Dev Tooling:** Nodemon, dotenv

---

## 📁 Project Structure

```
controllers/    # Request handlers / business logic
models/         # Mongoose schemas & models
routes/         # Express route definitions
views/          # EJS templates
public/         # Static assets & compiled CSS
uploads/        # Uploaded property images
utils/          # Helper / utility modules
app.js          # Application entry point
```

---

## 🔐 Environment Variables

Create a `.env` file in the project root:

```env
DB_PATH=<your_mongodb_connection_string>
PORT=5000
```

---

## ⚙️ Installation & Run

### 1️⃣ Install dependencies

```bash
npm install
```

### 2️⃣ Start development mode (server + Tailwind watcher)

```bash
npm start
```

### 3️⃣ Open in browser

```
http://localhost:5000
```

---

## 🌐 Main Routes

### 🔑 Auth

* `GET /login`
* `POST /login`
* `POST /logout`
* `GET /signup`
* `POST /signup`

### 👤 Store / User

* `GET /`
* `GET /homes`
* `GET /homes/:homeId`
* `GET /bookings`
* `GET /favourites`
* `POST /favourites`
* `POST /favourites/delete/:homeId`

### 🏡 Host (Protected)

* `GET /host/add-home`
* `POST /host/add-home`
* `GET /host/host-home-list`
* `GET /host/edit-home/:homeId`
* `POST /host/edit-home`
* `POST /host/delete-home/:homeId`

---

## 🚧 Current Status

This codebase is under **active development**. Upcoming improvements may include:

* 📚 Better API documentation & route coverage
* ⚠️ Improved centralized error handling & logging
* 👥 Role-based authorization enhancements
* 🧪 Automated test coverage
* 🔒 Security hardening (session & cookie configuration)


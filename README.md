# 🏡 Airbnb Backend

## Overview

This is a **backend-focused Airbnb-style application** built with **Node.js, Express, and MongoDB** following the MVC architectural pattern. The application provides authentication and authorization workflows, session-based user management, image upload handling, and CRUD operations for property listings and user favourites.

The project was developed to implement **real-world backend engineering concepts**, including secure authentication, session persistence, route protection, request validation, file handling, and scalable application architecture. It emphasizes clean code organization, maintainability, and industry-standard backend development practices.

---

##  Key Features

*  Authentication with signup / login / logout flow.
*  Authorization using protected host routes.
*  Session management with cookies (`express-session`)
*  Persistent session storage in MongoDB (`connect-mongodb-session`).
*  Password hashing using `bcryptjs`.
*  File upload support for home photos using `multer`.
*  Validation and sanitization using `express-validator`.
*  CRUD-style operations for property listings.
*  Favourite management for users.
*  Server-side rendering with EJS templates.

---

##  Tech Stack

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

##  Project Structure

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

##  Environment Variables

Create a `.env` file in the project root:

```env
DB_PATH=<your_mongodb_connection_string>
PORT=5000
```

---

##  Installation & Run

### 1️. Install dependencies

```bash
npm install
```

### 2️. Start development mode (server + Tailwind watcher)

```bash
npm start
```

### 3. Open in browser

```
http://localhost:5000
```

---

##  Main Routes

### Auth

* `GET /login`
* `POST /login`
* `POST /logout`
* `GET /signup`
* `POST /signup`

### Store / User

* `GET /`
* `GET /homes`
* `GET /homes/:homeId`
* `GET /bookings`
* `GET /favourites`
* `POST /favourites`
* `POST /favourites/delete/:homeId`

### Host (Protected)

* `GET /host/add-home`
* `POST /host/add-home`
* `GET /host/host-home-list`
* `GET /host/edit-home/:homeId`
* `POST /host/edit-home`
* `POST /host/delete-home/:homeId`

---

##  Future Enhancements

Potential improvements and planned enhancements include:

* Enhanced user interface and improved user experience
* Expanded API documentation and developer guides
* Centralized error handling and structured logging
* Advanced role-based access control (RBAC)
* Automated testing and improved test coverage
* Additional security enhancements for sessions and cookies
* Search, filtering, and pagination for property listings
* Performance optimization and scalability improvements
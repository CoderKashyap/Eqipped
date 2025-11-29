# Eqipped - E-commerce App (Node.js + EJS)

A full-stack E-commerce Application built with Node.js, Express, EJS, and MongoDB, designed to manage orders, products, and users with real-time event updates for the admin dashboard.
This project demonstrates strong backend architecture, clean MVC structure, authentication, and Doc verification.

## Tech Stack

- **Frontend:** HTML, CSS, JavaScript, EJS, jQuery
- **Backend:** Node.js, Express.js
- **Database:** MongoDB, Mongoose
- **Real-Time:** WebSockets (event-driven updates)
- **Other Tools:** Multer, Bcrypt, JWT, Session Management

---

## Features

- User Authentication & Authorization
Secure login system with protected admin routes.

- Product Management
Add, update, delete, categorize, and upload product images.

- Order Management
Track orders, update order status, and view complete history.

- User Management
Admin can monitor and manage all registered users.

- Real-Time Admin Updates
New orders, product changes, and user events reflected instantly using WebSockets.

- Cart & Checkout System
Add/remove items, update quantities, and place final checkout.

- Server-Side Rendering
Fast and SEO-friendly UI with EJS templating.

---


## Project Structure

```dash
├── public/
│   ├── css/
│   ├── js/
│   └── uploads/                # Uploaded files (if any)
│
├── resources/
│   ├── views/                  # EJS templates
│   ├── css/                    # Tailwind / custom styles
│   └── js/
│       └── app.js              # hidden via .gitignore (frontend logic)
│
├── routes/                     # Entry route files only (logic hidden)
│   ├── web.js                  # hidden (contains API/web logic)
│   └── Paytm/                  # hidden
│
├── app/
│   ├── http/
│   │   ├── controllers/        # hidden
│   │   ├── middlewares/        # hidden
│   ├── models/                 # hidden
│   ├── config/                 # hidden
│   └── helpers/                # hidden
│
├── server.js                   # hidden
├── package.json
└── .gitignore
```


## Setup Instructions

```bash

1. Clone the repo:
git clone [https://github.com/CoderKashyap/Mern-Auth-Boilerplate.git](https://github.com/CoderKashyap/Eqipped.git)

2. Install frontend dependencies:
cd equipped
npm install

3. Create .env file

MONGO_URI=your_mongodb_uri
JWT_SECRET=your_secret
PORT=3300

4. Start backend server:
npm run dev
```



**API Documentation**

```bash

**Auth**

POST /register
Request: { "username": "testuser", "email": "test@mail.com", "password": "123456" }
Response:
302 Redirect → /login
Flash Message: "User Successfully Registered"
Event Emitted: eventEmitter.emit("userCreated", user)


POST /login

Request: { "email": "test@mail.com", "password": "123456" }
Response: 

1. If email or password is missing
302 Redirect → /login
Flash: "All fields are required"

2. If authentication fails (wrong credentials)
302 Redirect → /login
Flash: info.message   // usually "Invalid email or password"

3. If authentication succeeds
302 Redirect → / (or /customer/orders, /vendor, or /admin depending on user role)

4. If Logged in
302 Redirect → dashboard/home (based on user role)
Flash message: "Logged in successfully" (implicit)


```


# Why This Project Stands Out?

- Covers essential e-commerce workflows
- Shows strong backend + MVC experience
- Implements real-time event communication
- Includes authentication, image uploads, and complex CRUD operations
- Demonstrates real-world system architecture and code organization



# 🔐 React + Node.js Authentication (Login & Logout Flow)

This project is a simple **Login & Logout system** built with **React.js (frontend)** and **Node.js + SQLite (backend)**.  
It allows users to **register, log in, stay logged in via sessions, and log out securely**.

---

## 📌 Features
- Register with email & password  
- Login with stored credentials  
- Passwords securely hashed using **bcrypt**  
- Prevents duplicate email registration  
- Session-based authentication with cookies  
- Logout and clear session  
- SQLite database for persistent storage  
- (Optional) Protected `/dashboard` route  

---

## 🛠 Tech Stack
- **Frontend:** React.js  
- **Backend:** Node.js, Express.js  
- **Database:** SQLite  
- **Authentication:** express-session, cookie-parser, bcrypt  

---

## 📂 Project Structure
react-node-auth/
│── backend/ # Node.js + Express backend (API + SQLite)
│── frontend/ # React.js frontend
│── README.md # Project documentation

yaml
Copy code

---

## ⚙️ Setup & Installation

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/<your-username>/react-node-auth.git
//cd react-node-auth

2️⃣ Backend Setup

//cd backend
//npm install

** Create database (if not auto-created):

// node db.js

** Start backend server **

//npm start
*** Runs on http://localhost:5000 ***

3️⃣ Frontend Setup

//cd ../frontend
//npm install
//npm start
Runs on http://localhost:3000

🔑 API Endpoints
*** Register User ***
POST /api/register
Request body:

{
  "email": "user@example.com",
  "password": "mypassword"
}

*** Login User ***
POST /api/login
** Request body:
{
  "email": "user@example.com",
  "password": "mypassword"
}

*** Logout User ***
POST /api/logout

Get Current Session User
GET /api/session

***🗄 Database Schema ***
Table: users

*** sql ***
CREATE TABLE users (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  email TEXT UNIQUE,
  password TEXT
);

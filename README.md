┌──────────────────────────────────────────────┐
│                                              │
│               🌍 GlobalAuth                  │
│                                              │
│ Enterprise Authentication Platform           │
│                                              │
│ Spring Boot • React • JWT • OAuth2           │
│                                              │
└──────────────────────────────────────────────┘

![GitHub last commit](https://img.shields.io/github/last-commit/divyansh1727/GlobalAuth?style=for-the-badge)
![GitHub repo size](https://img.shields.io/github/repo-size/divyansh1727/GlobalAuth?style=for-the-badge)
![GitHub stars](https://img.shields.io/github/stars/divyansh1727/GlobalAuth?style=for-the-badge)

# 🌍 GlobalAuth

![Java](https://img.shields.io/badge/Java-21-orange?style=for-the-badge&logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-4.x-6DB33F?style=for-the-badge&logo=springboot)
![React](https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?style=for-the-badge&logo=typescript)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Neon-336791?style=for-the-badge&logo=postgresql)
![JWT](https://img.shields.io/badge/JWT-Authentication-black?style=for-the-badge&logo=jsonwebtokens)


> A production-ready full-stack Authentication & Authorization platform built with **Spring Boot**, **React**, **TypeScript**, **Spring Security**, **JWT**, **OAuth2**, **PostgreSQL**, and **Cloudinary**.

GlobalAuth is a modern authentication system that provides secure user management with email/password authentication, Google and GitHub OAuth, JWT-based authorization, refresh token authentication, profile management, password updates, profile image uploads, and account deletion.

The application follows industry-standard authentication practices using **Spring Security**, **JWT access tokens**, **Refresh Tokens stored in HttpOnly Cookies**, and a clean separation between frontend and backend services.

---

## 🚀 Live Demo

### Frontend

> https://global-authapp.vercel.app

### Backend API

> https://globalauthbackend.onrender.com

---

## ✨ Features

### 🔐 Authentication

* User Registration
* Email & Password Login
* Secure Logout
* JWT Access Token Authentication
* Refresh Token Authentication
* HttpOnly Secure Cookies

### 🌐 OAuth Login

* Google OAuth 2.0
* GitHub OAuth 2.0
* Automatic account creation for first-time OAuth users

### 👤 User Management

* View Profile
* Edit Profile Information
* Upload Profile Picture
* Cloudinary Image Storage
* Change Password
* Delete Account

### 🛡 Security

* Spring Security
* BCrypt Password Encryption
* Role-Based Authorization
* Protected REST APIs
* Global Exception Handling

### ☁ Cloud Integration

* Cloudinary Image Upload
* PostgreSQL (Neon)
* Render Deployment
* Vercel Deployment

---

## 🛠 Tech Stack

### Backend

* Java 21
* Spring Boot
* Spring Security
* Spring Data JPA
* Hibernate
* JWT
* OAuth2 Client
* PostgreSQL
* Maven

### Frontend

* React
* TypeScript
* Vite
* Tailwind CSS
* shadcn/ui
* Zustand
* Axios
* React Hot Toast
* Framer Motion

### Cloud & Deployment

* Render
* Vercel
* Neon PostgreSQL
* Cloudinary

---

# 🏗 Project Structure

```text
GlobalAuth
│
├── Auth-app-frontend
│   ├── src
│   ├── public
│   ├── package.json
│   └── vite.config.ts
│
├── Auth-app-backend
│   ├── src
│   ├── pom.xml
│   ├── Dockerfile
│   └── ...
│
└── README.md
```

---

# 🏛 System Architecture

```mermaid
flowchart TD

    A["React + TypeScript Frontend"]
    B["Axios API Client"]
    C["Spring Security"]
    D["JWT Authentication Filter"]
    E["REST Controllers"]
    F["Service Layer"]
    G["Spring Data JPA"]
    H["PostgreSQL (Neon)"]
    I["Cloudinary"]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G --> H
    F --> I
```

---

# 🔐 Authentication Flow

```mermaid
sequenceDiagram

    participant User
    participant Frontend
    participant Backend
    participant Database

    User->>Frontend: Login
    Frontend->>Backend: POST /login
    Backend->>Database: Validate User
    Database-->>Backend: User Details
    Backend-->>Frontend: Access Token + Refresh Cookie
    Frontend->>Backend: Protected API Request
    Backend-->>Frontend: Protected Data
```
## 📸 Application Screenshots

### 🏠 Home Page
Modern Landing Page

![Home](screenshots/home.png)

---

### 🔑 Login
Secure User Login

![Login](screenshots/login.png)

---

### 📝 Sign Up
User Registration

![Sign Up](screenshots/signup.png)

---

### 📊 Dashboard
User Dashboard

![Dashboard](screenshots/dashboard.png)

---

### 👤 User Profile
Profile Management

![Profile](screenshots/profile.png)

---

### 🖼️ Update Profile Picture
Profile Picture Upload

![Update Profile Picture](screenshots/update-picture.png)

---

### 🗑️ Delete Account (Local User)
Password Verification

Users registered with email/password must confirm their password before deleting their account.

![Delete Local](screenshots/delete-local.png)

---

### 🌐 Delete Account (OAuth User)
OAuth Account Deletion

Users authenticated with Google or GitHub can securely delete their account without entering a password.

![Delete OAuth](screenshots/delete-oauth.png)


```
## 📡 REST API Endpoints

### Authentication APIs

| Method | Endpoint                | Description                  |
| ------ | ----------------------- | ---------------------------- |
| POST   | `/api/v1/auth/register` | Register a new user          |
| POST   | `/api/v1/auth/login`    | Login using email & password |
| POST   | `/api/v1/auth/refresh`  | Generate a new access token  |
| POST   | `/api/v1/auth/logout`   | Logout user                  |

### User APIs

| Method | Endpoint                             | Description          |
| ------ | ------------------------------------ | -------------------- |
| GET    | `/api/v1/users/{id}`                 | Get user details     |
| PUT    | `/api/v1/users/{id}`                 | Update profile       |
| POST   | `/api/v1/users/{id}/image`           | Upload profile image |
| POST   | `/api/v1/users/{id}/change-password` | Change password      |
| DELETE | `/api/v1/users/{id}/delete-account`  | Delete account       |

---

## ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/divyansh1727/GlobalAuth.git
cd GlobalAuth
```

### Frontend

```bash
cd Auth-app-frontend
npm install
npm run dev
```

### Backend

```bash
cd Auth-app-backend
./mvnw spring-boot:run
```

---

## 🔑 Environment Variables

### Backend

```env
SPRING_DATASOURCE_URL=
SPRING_DATASOURCE_USERNAME=
SPRING_DATASOURCE_PASSWORD=

JWT_SECRET=

GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=

GITHUB_CLIENT_ID=
GITHUB_CLIENT_SECRET=

CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=
```

### Frontend

```env
VITE_API_BASE_URL=
```

---

## 🚀 Future Improvements

* Email Verification
* Forgot Password
* Two-Factor Authentication (2FA)
* Admin Dashboard
* Audit Logging
* Docker Compose Support
* CI/CD Pipeline
* Unit & Integration Tests

---

## 👨‍💻 Author

**Divyansh Singh**

If you found this project helpful, consider giving it a ⭐ on GitHub.


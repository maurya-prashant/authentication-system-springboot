# 🔐 Authentication System (Spring Boot)

A **complete, production-oriented authentication & authorization system** built using Spring Boot.
This project is designed for **deep learning of backend architecture**, not just implementation.

---

## 🎯 Purpose of This Project

* Understand **Spring Boot ecosystem (end-to-end)**
* Learn **Authentication vs Authorization**
* Build a **scalable backend architecture**
* Implement **JWT-based stateless security**
* Practice **real-world backend design patterns**

---

## 🚀 Tech Stack

* **Java 21**
* **Spring Boot 3**
* **Spring Security**
* **Spring Data JPA (Hibernate)**
* **H2 (Dev) → MySQL (Production)**
* **JWT (io.jsonwebtoken)**
* **Lombok**
* **Spring Validation**
* **Swagger / OpenAPI**

---

## 📂 Project Structure

```text
src/main/java/com/authsystem/

├── controller/        # REST APIs (entry point)
├── service/           # Business logic layer
├── repository/        # Database access layer
├── entity/            # Database models (JPA entities)
├── dto/               # Request/Response objects
├── security/          # JWT, filters, authentication logic
├── config/            # App configuration (Security, Beans)
├── exception/         # Global error handling
│   └── handler/       # Centralized exception handlers
```

---

## 🧠 Architecture Overview

```text
Client (Postman / Frontend)
        ↓
Controller  → handles HTTP requests
        ↓
Service     → business logic
        ↓
Repository  → database interaction
        ↓
Database
```

---

## 🔑 Core Concepts Covered

### 🔐 Authentication

* Verifying **who the user is**
* Email + Password login
* JWT token generation

---

### 🛡️ Authorization

* Determining **what the user can do**
* Role-based access:

  * ROLE_USER
  * ROLE_ADMIN

---

### 🔄 Stateless Security

* No server-side session storage
* JWT token used in every request

---

## 🧩 Features Roadmap

---

### 🟢 Phase 1: Foundation

* [ ] Project setup & structure
* [ ] User entity & repository
* [ ] Registration API
* [ ] Password hashing (BCrypt)
* [ ] Input validation

---

### 🟡 Phase 2: Authentication (JWT)

* [ ] Login API
* [ ] JWT token generation
* [ ] JWT utility class
* [ ] Security filter (request interception)
* [ ] Spring Security configuration

---

### 🔵 Phase 3: Authorization

* [ ] Role-based access control
* [ ] Protected endpoints
* [ ] Method-level security (`@PreAuthorize`)

---

### 🟣 Phase 4: Token Management

* [ ] Access Token (short-lived)
* [ ] Refresh Token (long-lived)
* [ ] Token rotation
* [ ] Logout functionality

---

### 🟠 Phase 5: User Account Features

* [ ] Email verification
* [ ] Forgot password
* [ ] Reset password

---

### 🔴 Phase 6: Security Enhancements

* [ ] Rate limiting (basic)
* [ ] Account lock after failed attempts
* [ ] Secure headers
* [ ] Input sanitization

---

### ⚫ Phase 7: Advanced Features

* [ ] Multi-device session management
* [ ] Login activity tracking
* [ ] Audit logging
* [ ] Optional: OAuth (Google login)

---

## 🔄 Authentication Flow

```text
1. User registers → data stored with hashed password
2. User logs in → receives JWT token
3. Client sends token in Authorization header
4. JWT filter validates token
5. Request proceeds if valid
```

---

## 📡 API Design (Versioned)

### Base URL:

```text
/api/v1/
```

---

### 🔑 Authentication APIs

| Method | Endpoint              | Description          |
| ------ | --------------------- | -------------------- |
| POST   | /api/v1/auth/register | Register new user    |
| POST   | /api/v1/auth/login    | Login user           |
| POST   | /api/v1/auth/refresh  | Refresh access token |
| POST   | /api/v1/auth/logout   | Logout user          |

---

### 👤 User APIs

| Method | Endpoint             | Description         |
| ------ | -------------------- | ------------------- |
| GET    | /api/v1/user/profile | Get user profile    |
| PUT    | /api/v1/user/update  | Update user details |

---

### 🛡️ Admin APIs

| Method | Endpoint            | Description   |
| ------ | ------------------- | ------------- |
| GET    | /api/v1/admin/users | Get all users |
| DELETE | /api/v1/admin/{id}  | Delete user   |

---

## 🧪 Testing

Swagger UI:

```text
http://localhost:8080/swagger-ui.html
```

---

## 🔐 Security Implementation Details

* Password hashing using **BCrypt**
* JWT signing & validation
* Secure endpoints using Spring Security
* CSRF disabled (for stateless APIs)
* Stateless session management

---

## 🗄️ Database Design (Planned)

Tables:

* `users`
* `roles` (optional)
* `refresh_tokens`
* `password_reset_tokens`
* `email_verification_tokens`

---

## ⚙️ Configuration Highlights

* `SecurityConfig` → defines access rules
* `PasswordEncoder` → BCrypt bean
* JWT secret stored securely

---

## 🧠 Learning Outcomes

By completing this project, you will:

* Understand **layered architecture**
* Learn **how Spring Security works internally**
* Implement **real-world authentication systems**
* Gain confidence in **backend development**

---

## ⚠️ Notes

* Built step-by-step for learning
* Avoid copying code blindly
* Focus on understanding flow between layers

---

## 🚀 Future Improvements

* Dockerization
* Deployment (AWS / Render / Railway)
* CI/CD pipeline
* Integration testing

---

## 👨‍💻 Author

Prashant Maurya

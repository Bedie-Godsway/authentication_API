# 🔐 Authentication System API

A secure RESTful Authentication API built with Node.js, Express.js, MongoDB, and JWT. This API provides user registration, login, authentication, and protected route functionality.

---

## 🚀 Features

- User Registration
- User Login
- Password Hashing with bcrypt
- JWT Authentication
- Protected Routes
- MongoDB Database Integration
- Environment Variable Configuration
- Error Handling Middleware

---

## 🛠️ Technologies Used

- Node.js
- Express.js
- MongoDB Atlas
- Mongoose
- JSON Web Token (JWT)
- bcryptjs
- dotenv
- Nodemon

---

## 📂 Project Structure

```text
backend/
│
├── config/
│   └── database.js
│
├── controllers/
│   └── userController.js
│
├── middlewares/
│   └── userMiddleware.js
│
├── models/
│   └── userModel.js
│
├── routes/
│   └── userRoutes.js
│
├── .env
├── .gitignore
├── package.json
├── server.js
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Bedie-Godsway/authentication_API.git
```

### 2. Navigate into the Project Directory

```bash
cd authentication_API
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Create Environment Variables

Create a `.env` file in the root directory and add:

```env
PORT=5000

MONGO_URI=your_mongodb_connection_string

JWT_SECRET=your_jwt_secret
```

### 5. Start the Development Server

```bash
npm run dev
```

Server should start on:

```text
http://localhost:5000
```

---

## 🔑 API Endpoints

### Register User

**POST**

```http
/api/auth/register
```

#### Request Body

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "password123"
}
```

---

### Login User

**POST**

```http
/api/auth/login
```

#### Request Body

```json
{
  "email": "john@example.com",
  "password": "password123"
}
```

---

### Get User Profile (Protected)

**GET**

```http
/api/auth/profile
```

#### Authorization Header

```http
Authorization: Bearer YOUR_JWT_TOKEN
```

---

## 🔐 Authentication Flow

1. User registers an account.
2. Password is hashed before storage.
3. User logs in using email and password.
4. Server verifies credentials.
5. JWT token is generated and returned.
6. Client stores the token.
7. Token is sent in the Authorization header for protected routes.
8. Middleware verifies the token before granting access.

---

## 🧪 Testing with Postman

### Register

```http
POST http://localhost:5000/api/auth/register
```

### Login

```http
POST http://localhost:5000/api/auth/login
```

### Protected Route

```http
GET http://localhost:5000/api/auth/profile
```

Add:

```http
Authorization: Bearer YOUR_TOKEN
```

to the request headers.

---

## 🌐 Deployment

This API can be deployed using:

- Render
- Railway
- AWS
- DigitalOcean

---

## 🤝 Contributing

Contributions are welcome.

1. Fork the repository
2. Create a feature branch

```bash
git checkout -b feature-name
```

3. Commit your changes

```bash
git commit -m "feat: add new feature"
```

4. Push to GitHub

```bash
git push origin feature-name
```

5. Open a Pull Request

---

## 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Godsway Bedie**

- GitHub: https://github.com/Bedie-Godsway
- Email: bediegodsway@gmail.com


---

⭐ If you found this project useful, consider giving it a star.

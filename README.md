# DecodeLabs Project 3 – Database Integration API

A RESTful User Management API built with Node.js, Express.js, MongoDB, and Mongoose. This project demonstrates database integration, CRUD operations, input validation, error handling, filtering, searching, and pagination.

## 🚀 Features

- Create, Read, Update, and Delete (CRUD) users
- MongoDB database integration using Mongoose
- RESTful API architecture
- Request validation using Express Validator
- Unique email constraint
- Search users by name or email
- Filter users by role
- Pagination support
- Global error handling
- Environment variable configuration
- CORS support

---

## 🛠️ Tech Stack

- Node.js
- Express.js
- MongoDB
- Mongoose
- Express Validator
- dotenv
- CORS

---

## 📂 Project Structure

```
decodelabs-p3/
│
├── config/
│   └── db.js
│
├── models/
│   └── User.js
│
├── routes/
│   └── users.js
│
├── .env.example
├── .gitignore
├── package.json
└── server.js
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/decodelabs-p3-database-integration.git
cd decodelabs-p3-database-integration
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

Create a `.env` file in the root directory:

```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
NODE_ENV=development
```

### 4. Start the Server

Development Mode:

```bash
npm run dev
```

Production Mode:

```bash
npm start
```

Server will run on:

```text
http://localhost:5000
```

---

## 📌 API Endpoints

### Create User

```http
POST /api/users
```

Request Body:

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "age": 25,
  "role": "student"
}
```

---

### Get All Users

```http
GET /api/users
```

Query Parameters:

| Parameter | Description |
|------------|------------|
| role | Filter by role |
| search | Search by name/email |
| page | Page number |
| limit | Records per page |

Example:

```http
GET /api/users?role=student&page=1&limit=10
```

---

### Get User by ID

```http
GET /api/users/:id
```

Example:

```http
GET /api/users/685f123abc456def78901234
```

---

### Update User (Full Update)

```http
PUT /api/users/:id
```

---

### Update User (Partial Update)

```http
PATCH /api/users/:id
```

Example:

```json
{
  "role": "admin"
}
```

---

### Delete User

```http
DELETE /api/users/:id
```

---

## ✅ Validation Rules

| Field | Validation |
|---------|------------|
| Name | Required, 2–50 characters |
| Email | Required, valid email format, unique |
| Age | Required, minimum 18 |
| Role | student, instructor, admin |

---

## 📊 Database Schema

```javascript
{
  name: String,
  email: String,
  age: Number,
  role: String,
  isActive: Boolean,
  createdAt: Date,
  updatedAt: Date
}
```

---

## 🔒 Error Handling

The API handles:

- Invalid input data
- Duplicate email addresses
- Invalid MongoDB ObjectIds
- Missing resources
- Internal server errors

---

## 🧪 Testing

You can test the API using:

- Postman
- Thunder Client
- Insomnia

---


## 🎯 Learning Outcomes

This project demonstrates:

- MongoDB Database Integration
- Mongoose Schema Design
- REST API Development
- CRUD Operations
- Validation Middleware
- Error Handling
- Search & Pagination
- Backend Development Best Practices

---

## 👨‍💻 Author

**Bhumi Gupta**

- GitHub: https://github.com/Bhumigupta12345


---

## 📜 License

This project is developed for learning and educational purposes under the DecodeLabs Full Stack Development Program.

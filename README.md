# 📇 Contact App

A **full-stack backend application** for managing personal and professional contacts. This app provides a secure and efficient way to **store, update, and retrieve contacts** with built-in authentication and API endpoints.

---

## 🚀 Features

✅ **User Authentication** – Secure login & registration with JWT  
✅ **User-Specific Contacts** – Each user manages their own contacts  
✅ **CRUD Operations** – Create, Read, Update, and Delete contacts  
✅ **Pagination, Sorting & Filtering** – Efficient data retrieval  
✅ **RESTful API** – Well-structured API endpoints for seamless integration  
✅ **MongoDB Database** – Efficient data storage & retrieval  
✅ **Validation & Error Handling** – Ensures data integrity and security  
✅ **Secure Data Management** – Password hashing
✅ **Session Management** – Token refresh & logout functionality

---

## 📂 Project Structure

````
📺 Contact-App
├── constants/            # Application-wide constants
├── controllers/          # Business logic for contacts & users
├── db/                   # Database connection & models
│   ├── models/           # Database schemas
├── middlewares/          # Authentication & validation layers
├── routers/              # API route handlers
├── services/             # Service layer for business logic
├── templates/            # Email templates (e.g., reset-password-email.html)
├── utils/                # Helper functions
├── validation/           # Input validation logic
├── index.js              # Main entry point
├── server.js             # Server configuration & setup
└── README.md             # Project documentation

---

## 🔧 Installation & Setup

```bash
# Clone the repository
git clone https://github.com/your-username/contact-app.git
cd contact-app

# Install dependencies
npm install

# Set up environment variables (create a .env file)
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key

# Start the server
npm start
````

---

## 🏗️ API Endpoints

### **User Authentication**

- `POST /api/auth/register` → Register a new user
- `POST /api/auth/login` → Authenticate user & get token
- `POST /api/auth/logout` → Logout user & invalidate token
- `POST /api/auth/refresh` → Refresh session with new token
- `POST /api/auth/request-reset-email` → Request password reset email
- `POST /api/auth/reset-password` → Reset password

### **Contacts Management**

- `GET /api/contacts` → Fetch all user-specific contacts (supports pagination, sorting, filtering)
- `POST /api/contacts` → Add a new contact
- `GET /api/contacts/:contactId` → Fetch a single contact
- `PUT /api/contacts/:contactId` → Update contact details
- `PATCH /api/contacts/:contactId` → Partially update contact
- `DELETE /api/contacts/:contactId` → Delete a contact

---

## 📌 Usage

```javascript
fetch('/api/contacts', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
    Authorization: 'Bearer YOUR_TOKEN',
  },
  body: JSON.stringify({ name: 'John Doe', email: 'john@example.com' }),
})
  .then((response) => response.json())
  .then((data) => console.log(data));
```

---

## 🔒 Security Measures

- **Password Hashing** – Uses bcrypt for secure password storage
- **JWT Authentication** – Protects routes with token-based authentication
- **Input Validation** – Prevents invalid or malicious data entries
- **Session Management** – Supports logout & token refresh functionality

---

## 🤝 Contributing

Want to improve this project? Feel free to **fork**, create a new branch, and submit a **pull request**! 🚀

---

## ⭐ Acknowledgments

- **Node.js & Express** for backend development
- **MongoDB & Mongoose** for database management
- **JWT & bcrypt** for authentication & security

---

### 📇 Ready to manage your contacts? **Fork & start coding!** 🔥

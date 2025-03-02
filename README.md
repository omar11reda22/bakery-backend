# Multi-Actor E-commerce System with Inventory Management

## About the Project
This system is designed to manage an **E-commerce Platform** integrated with an **Inventory Management System** using **Angular (Frontend)** and **Node.js (Backend)**. The system supports three main actors:

- **Customers**: Browse products, add items to the cart, and complete purchases.
- **Sellers**: Manage their product listings, process orders, and track sales analytics.
- **Admins**: Control stock in branches, handle requests, manage users, and oversee inventory.

## Features
### General Features:
- **User Authentication** (Customers, Sellers, Admins)
- **Product Catalog with Search & Filter**
- **Shopping Cart & Checkout**
- **Order Tracking**
- **Dashboard for Sellers & Admins**
- **Stock Management per Branch**
- **Restock Requests from Branches**
- **Admin Control over Inventory and Orders**
- **Responsive UI (Desktop, Mobile, Tablet Support)**

---

## Tech Stack
### **Frontend:** Angular
- Angular 16+
- Bootstrap 5
- RxJS (State Management)
- Angular Router
- Chart.js (Data Visualization)

### **Backend:** Node.js (Express.js)
- Express.js
- MongoDB (Mongoose ORM)
- JSON Web Token (JWT) for Authentication
- ImageKit for Image Storage
- Bcrypt for Password Hashing

---

## Installation & Setup
### **Backend Setup (Node.js)**
1. Clone the backend repo:
   ```sh
   git clone https://github.com/yourusername/backend-repo.git
   cd backend-repo
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Configure `.env` file:
   ```
   PORT=5000
   MONGO_URI=mongodb+srv://<db_username>:<db_password>@yourcluster.mongodb.net/
   JWT_SECRET=your_secret_key
   IMAGEKIT_PUBLIC_KEY=your_public_key
   IMAGEKIT_PRIVATE_KEY=your_private_key
   IMAGEKIT_ENDPOINT_URL=https://ik.imagekit.io/your_imagekit
   ```
4. Run the server:
   ```sh
   npm start
   ```

### **Frontend Setup (Angular)**
1. Clone the frontend repo:
   ```sh
   git clone https://github.com/yourusername/frontend-repo.git
   cd frontend-repo
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Configure environment file (`src/environments/environment.ts`):
   ```ts
   export const environment = {
     production: false,
     apiUrl: 'http://localhost:5000/api'
   };
   ```
4. Run the Angular app:
   ```sh
   ng serve
   ```

---

## API Documentation (Backend)
### **User Authentication**
#### **Register a new user**
```http
POST /api/auth/register
```
**Request Body:**
```json
{
  "username": "JohnDoe",
  "email": "johndoe@example.com",
  "password": "securepassword"
}
```

#### **Login**
```http
POST /api/auth/login
```
**Request Body:**
```json
{
  "email": "johndoe@example.com",
  "password": "securepassword"
}
```
**Response:**
```json
{
  "token": "your_jwt_token"
}
```

---

### **Products**
#### **Get all products**
```http
GET /api/products
```

#### **Get a single product**
```http
GET /api/products/:id
```

---

### **Inventory Management (Admin)**
#### **Get all branches**
```http
GET /api/branches
```
#### **Approve a stock request**
```http
PUT /api/requests/:id/approve
```

---

## Contributing
1. Fork the repository.
2. Create a new branch (`feature-branch`).
3. Commit your changes.
4. Push to your branch and create a pull request.

## License
This project is licensed under the MIT License.

---

## Contact
For any inquiries, contact: **your.email@example.com**


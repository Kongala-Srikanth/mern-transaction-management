# **Transaction Management System**

## **Frontend**

A web application for managing user transactions, including features for transaction history, profile management, and secure authentication. Built using React.js for the frontend and a backend API for transaction and user data management.

---

## **Features**

- **User Authentication:**
  - Login and register with JWT-based authentication.
  - Protected routes to secure user data.

- **User Profile:**
  - View user details such as User ID, email, and account balance.
  - Logout functionality.

- **Transaction Management:**
  - View a detailed transaction history.
  - Update transaction status dynamically.
  - Responsive design for a seamless experience on any device.

- **Routing:**
  - Intuitive navigation using React Router.

---

## **Technologies Used**

### **Frontend:**
- React.js
- React Router
- `js-cookie` for managing authentication tokens
- `react-loader-spinner` for loading animations
- CSS for styling and responsiveness

### **Backend:**
- API endpoints for authentication and transaction management

---

## **Installation and Setup**

### **Prerequisites**
- Node.js installed
- A package manager (`npm` or `yarn`)

### **Steps**

1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd transaction-management ```
2. Install dependencies:

   ```bash
   npm install ```
3. Set up environment variables:
- Create a .env file in the root directory.
- Add the API URL and other required configurations:

   ```bash
   REACT_APP_API_URL=https://transactions-management-backend-u1fz.onrender.com ```
4. Run the application:

   ```bash
   npm start ```
5. Open your browser and navigate to http://localhost:3000.

## **Usage**

### **Login/Register:**
- Use the `/login` or `/register` routes to authenticate.

### **View Profile:**
- Navigate to `/profile` to see user details.

### **Transaction Management:**
- View transaction history at `/transactions`.
- Click on a transaction to see more details or update its status.

---

## **API Endpoints**

### **User Details:**
- `GET /user/account`  
  Returns the authenticated user's account information.

### **Transaction History:**
- `GET /api/transactions/:userId`  
  Fetches transaction details for a specific user.

### **Update Transaction Status:**
- `PUT /api/transactions/:transactionId`  
  Updates the status of a specific transaction.

<br/> <br/> <br/> <br/> <br/> <br/> <br/> <br/> <br/>

## **Backend**

This is a **Node.js**-based backend project for managing bank transactions, including user registration, login, and CRUD operations for transactions. The application uses **Express.js**, **MongoDB**, and **JWT** for secure and efficient data handling.

## Features

- **User Registration**: Register new users with hashed passwords.
- **User Login**: Authenticate users and generate JWT tokens.
- **Transactions**:
  - Create transactions (Deposit/Withdrawal).
  - Update transaction status.
  - Retrieve transaction details.
- **Secure API Endpoints**: Protected routes using JWT authentication.
- **Error Handling**: Robust error handling for all endpoints.

## Tech Stack

- **Backend Framework**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Tokens)
- **Password Hashing**: bcrypt
- **Unique IDs**: uuid
- **Environment Variables**: dotenv

## Installation

## 1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <project-directory>
  ```
### 2. Install dependencies:
```bash
npm install
```
### 3. Create a .env file in the root directory with the following content:
```bash
DB_USER=<your-db-user>
DB_PASSWORD=<your-db-password>
DB_CLUSTER=<your-db-cluster>
DB_NAME=<your-database-name>
JWT_SECRET=<your-jwt-secret>
```
### 4. Start the server:
```bash
node <file-name>.js
```
Replace <file-name> with the name of your server file.

## API Endpoints
### 1. Register New User
- Endpoint: /register
- Method: POST
- Request Body:
```bash
{
  "username": "Srikanth",
  "email": "srikanth@gmail.com",
  "password": "srikanth"
}
```
- **Response**:
```bash
{
  "message": "User Successfully Registered"
}
```
### 2. Login
- Endpoint: /login
- Method: POST
- Request Body:
```bash
{
  "email": "srikanth@gmail.com",
  "password": "srikanth"
}
```
- **Response**:
```bash
{
  "jwtToken": "<token>",
  "userId": "<user-id>"
}
```

## Transaction Endpoints
### 3. Create Transaction
- URL: /api/transactions
- Method: POST
- Headers: Authorization: Bearer <jwt-token>
- Request Body:
```bash
{
  "amount": 500,
  "transaction_type": "DEPOSIT",
  "user": "<user-id>"
}
```
- **Response**:
```bash
{
  "message": "Transaction successfully done"
}
```

### 4. Get User Transactions
- URL: /api/transactions/:id
- Method: GET
- Headers: Authorization: Bearer <jwt-token>
- **Response**:
```bash
{
  "transactions": [/* transactions array */]
}
```

### 5. Update Transaction Status
- URL: /api/transactions/:id
- Method: PUT
- Headers: Authorization: Bearer <jwt-token>
- Request Body:
```bash
{
  "status": "COMPLETED"
}
```
- **Response**:
```bash
{
  "message": "Successfully Status Updated"
}
```

### 6. Get Transaction by ID
- URL: /api/transaction/:id
- Method: GET
- Headers: Authorization: Bearer <jwt-token>
- **Response**:
```bash
{
  /* transaction details */
}
```


## Dependencies
- express: Fast, unopinionated web framework
- cors: Enable Cross-Origin Resource Sharing
- uuid: Generate unique identifiers
- mongodb: MongoDB driver for Node.js
- jsonwebtoken: Authenticate and secure API
- bcrypt: Hash passwords for secure storage
- dotenv: Manage environment variables

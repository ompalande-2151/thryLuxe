# 🛍️ thryLuxe - Premium Lifestyle E-commerce App

**thryLuxe** is a full-stack e-commerce web application built with the MERN stack (MongoDB, Express, React, Node.js). It supports complete product browsing, shopping cart, authentication, and order placement with address management.

---

## 🚀 Features

### 👤 User Side

- Register & Login (JWT Auth)
- Browse product categories
- Add to cart with live quantity management
- Save delivery address
- Place order (Cash on Delivery)
- View order history

### 🛒 Seller/Admin Side

- Seller login
- Add new products with images
- Toggle stock availability
- View all orders (seller dashboard)

---

## 🧩 Tech Stack

| Layer        | Technology          |
| ------------ | ------------------- |
| Frontend     | React, TailwindCSS  |
| State Mgmt   | React Context API   |
| Backend      | Express.js, Node.js |
| Database     | MongoDB             |
| Auth         | JWT with Cookies    |
| Image Upload | Multer              |

---

## 📂 Project Structure

```
thryLuxe/
├── client/           # React frontend
│   ├── components/   # UI Components
│   ├── pages/        # Page-level components
│   ├── assets/       # Images & constants
│   ├── context/      # Global AppContext
│   └── App.js        # Root component
│
├── server/           # Express backend
│   ├── controllers/  # Logic for API endpoints
│   ├── models/       # Mongoose schemas
│   ├── routes/       # API route definitions
│   ├── middlewares/  # Auth & utilities
│   ├── configs/      # Multer, DB config
│   └── server.js     # Entry point
│
└── README.md         # This file (Project overview)
```

---

## ⚙️ Setup Instructions

### 🔑 Prerequisites

- Node.js
- MongoDB (local or cloud e.g. Atlas)
- Git

### 1. Clone the Repo

```bash
 https://github.com/ompalande-2151/thryLuxe.git
cd thryLuxe
```

### 2. Setup Backend

```bash
cd server
npm install
```

Create a `.env` file in `server/` with the following:

```env
PORT=4000
MONGO_URL=mongodb://localhost:27017/thryluxe
JWT_SECRET=your_jwt_secret
NODE_ENV=development
```

Start the backend:

```bash
npm run server
```

### 3. Setup Frontend

```bash
cd ../client
npm install
```

Create a `.env` file in `client/` with:

```env
VITE_BACKEND_URL=http://localhost:4000
VITE_CURRENCY=₹
```

Start the frontend:

```bash
npm run dev
```

---

<!--
## 📸 Screenshots

> You can add UI screenshots here:
- 🛍️ Product List
- 🧾 Order Summary
- 👤 Login/Register
- 🧰 Seller Dashboard -->

---

## 📦 API Endpoints Overview

### ✅ Auth

- `POST /api/user/register`
- `POST /api/user/login`
- `GET /api/user/is-auth`
- `POST /api/user/logout`

### 🛒 Products

- `POST /api/product/add` (Seller)
- `GET /api/product/list`
- `PUT /api/product/stock` (Toggle stock)

### 📦 Orders

- `POST /api/order/cod`
- `POST /api/order/user`
- `GET /api/order/seller`

### 📬 Address

- `POST /api/address/add`
- `GET /api/address/get`

### 🛍️ Cart

- `POST /api/cart/update`

---

## 🧑‍💻 Author

> Om palande

---

## 📝 Future Enhancements

- Online Payment (Razorpay)
- Order Cancellation & Refund
- Product Filter

---

## 📄 License

This project is licensed under [MIT License](LICENSE) — feel free to use and modify.

---

## 📣 Contact

For feedback, bugs, or contributions:
📧 Email: ompalande2151@gmail.com

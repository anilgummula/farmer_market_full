
# 🌾 Farmer Market Platform  

A **MERN stack web application** that connects **farmers** directly with **retailers/consumers**, eliminating intermediaries. Farmers can list their products and manage orders, while retailers can browse products, place orders, and monitor their purchases.  

---

## 🚀 Features  

### 👨‍🌾 Farmer  
- Login/Register securely.  
- Add new products with details (name, category, price, quantity, image).  
- View and manage listed products.  
- Manage incoming orders (Accept/Reject).  
- Dashboard with statistics:  
  - Total Orders  
  - Pending Orders  
  - Accepted/Rejected Orders  

### 🛒 Retailer  
- Login/Register securely.  
- Browse all listed products in the **Shop**.  
- Buy products from farmers.  
- Dashboard with statistics:  
  - Total Orders  
  - Completed/Pending Orders  

### 🔐 Authentication  
- JWT-based authentication.  
- Role-based access (Farmer / Retailer).  

### 🗄️ Backend APIs  
- Farmer APIs → Add Product, Manage Products, Manage Orders.  
- Retailer APIs → Browse Products, Buy Product, View Orders.  
- Authentication APIs → Register, Login, Profile.  

---

## 🏗️ Tech Stack  

### Frontend  
- React.js (Vite)  
- TailwindCSS for modern responsive UI  
- React Router DOM for navigation  
- Toast notifications for success/error handling  

### Backend  
- Node.js + Express.js  
- MongoDB (Cloud Cluster)  
- JWT for authentication  
- Multer (for image upload)  

### Deployment  
- Frontend → Netlify  
- Backend → Render  
- Database → MongoDB Atlas  

---

## 📂 Project Structure  

```
project/
├── backend/
│   ├── Controllers/
│   │   ├── AuthController.js
│   │   ├── FarmerController.js
│   │   └── RetailerController.js
│   ├── Middlewares/
│   │   ├── Auth.js
│   │   └── AuthValidation.js
│   ├── models/
│   │   ├── Product.js
│   │   ├── Order.js
│   │   └── User.js
│   ├── routes/
│   │   ├── Authrouter.js
│   │   ├── farmer.js
│   │   └── retailer.js
│   └── server.js
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── AddProductForm.jsx
│   │   │   ├── FarmerDashboard.jsx
│   │   │   ├── RetailerDashboard.jsx
│   │   │   ├── ShopComponent.jsx
│   │   │   └── NavBar.jsx
│   │   ├── utils/
│   │   │   └── index.js
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── index.html
```

---

## ⚡ Getting Started  

### 1. Clone the Repository  
```bash
git clone https://github.com/anilgummula/farmer_market_full.git
cd farmer_market_full
```

### 2. Setup Backend  
```bash
cd backend
npm install
```

Create a `.env` file in `/backend` with:  
```
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
```

Run backend:  
```bash
npm start
```

### 3. Setup Frontend  
```bash
cd frontend
npm install
```

Create `.env` file in `/frontend`:  
```
VITE_APP_API_BASE_URL=https://farmer-market-backend-xpxy.onrender.com
```

Run frontend:  
```bash
npm run dev
```

---

## 🌐 Deployment  
- **Frontend (Netlify):** `npm run build` → deploy `dist/` folder.  
- **Backend (Render):** connect repo & configure env variables.  
- **Database (MongoDB Atlas):** create cluster & connect using `MONGO_URI`.  

---


## 📜 License  
This project is licensed under the MIT License.  

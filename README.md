
# 🌾 GoFarm - Smart Farming Solution

![GoFarm Banner](./assets/banner.png)

## 🚀 Project Overview
GoFarm is a **full-stack smart farming platform** designed to empower farmers and buyers with advanced tools and insights. The platform includes:
- **AI/ML-based crop prediction** to help farmers make informed decisions.
- **AI voice assistant** for answering farming-related queries.
- A **marketplace** for farmers to sell crops and buyers to purchase them.
- A **shop** for farmers to buy farming-related products.
- **Data analytics and insights** for better crop management.

The project is built with:
- **Frontend**: TypeScript, React, Tailwind CSS
- **Backend**: Node.js, Express, MongoDB (MEN stack)
- **AI/ML**: Python, TensorFlow for crop prediction
- **Voice Assistant**: Integration with a natural language processing (NLP) API

---

## 🛠️ Tech Stack
![TypeScript](https://img.shields.io/badge/TypeScript-Frontend-blue?logo=typescript)
![React](https://img.shields.io/badge/React-18-blue?logo=react)
![Node.js](https://img.shields.io/badge/Node.js-Express-green?logo=node.js)
![MongoDB](https://img.shields.io/badge/MongoDB-Database-green?logo=mongodb)
![Python](https://img.shields.io/badge/Python-ML-orange?logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-AI/ML-orange?logo=tensorflow)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-CSS-blue?logo=tailwind-css)

---

## 📂 Project Structure

### **Frontend**
```
project/
├── .bolt/                  # Configuration files for Bolt (if used)
├── src/                    # Source code
│   ├── components/         # Reusable React components
│   ├── data/               # Static data or mock data
│   ├── hooks/              # Custom React hooks
│   ├── store/              # State management (e.g., Redux, Zustand)
│   ├── App.tsx             # Main application component
│   ├── index.css           # Global styles
│   ├── main.tsx            # Entry point for the application
│   ├── types.ts            # TypeScript type definitions
│   └── vite-env.d.ts       # Vite environment type definitions
├── .gitignore              # Files to ignore in Git
├── eslint.config.js        # ESLint configuration
├── index.html              # HTML template for the app
├── package-lock.json       # Lock file for dependencies
├── package.json            # Project dependencies and scripts
├── postcss.config.js       # PostCSS configuration
├── tailwind.config.js      # Tailwind CSS configuration
├── tsconfig.app.json       # TypeScript configuration for the app
└── README.md               # Project documentation (you're here!)
```

### **Backend**
```
backend/
├── controllers/            # Handles request logic
├── models/                 # Database models (MongoDB)
├── routes/                 # API routes
├── utils/                  # Utility functions
├── server.js               # Entry point for the backend
├── .env                    # Environment variables
└── package.json            # Backend dependencies and scripts
```

---

## 📦 Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/GoFarm.git
cd GoFarm
```

### 2️⃣ Install Dependencies
#### Backend
```bash
cd backend
npm install
```
#### Frontend
```bash
cd frontend
npm install
```

### 3️⃣ Set Up Environment Variables
Create a `.env` file in the `backend` folder and add:
```env
DB_URI=your_mongodb_url
API_KEY=your_api_key
WEATHER_API_KEY=your_weather_api_key
VOICE_ASSISTANT_API_KEY=your_nlp_api_key
```

### 4️⃣ Start the Application
#### ▶ Run Backend
```bash
cd backend
npm start
```
#### ▶ Run Frontend
```bash
cd frontend
npm run dev
```

---

## 🎯 Features

### **For Farmers**
✅ **AI Voice Assistant**: Answer farming-related queries using natural language processing.  
✅ **Crop Prediction**: AI/ML-based recommendations for the best crops to grow.  
✅ **Shop for Farmers**: Purchase farming-related products like seeds, fertilizers, and tools.  
✅ **Sell Crops**: List crops for sale on the marketplace.  
✅ **Dashboard**: View past crop analysis, growth trends, and task schedules.  
✅ **Market Insights**: Get real-time market trends and pricing for crops.  
✅ **Cart**: Manage purchases and orders.  

### **For Buyers**
✅ **Buy Crops**: Browse and purchase crops directly from farmers.  
✅ **Cart**: Manage orders and checkout.  
✅ **Farming Information**: Learn about farming practices and crop details.  

### **General**
✅ **Login/Register**: Secure authentication for farmers and buyers.  
✅ **Responsive Design**: Works seamlessly on desktop and mobile devices.  

---

## 🔗 API Endpoints

### **Authentication**
| Endpoint          | Method | Description                          |
|-------------------|--------|--------------------------------------|
| `/api/auth/register` | POST   | Register a new user (farmer or buyer) |
| `/api/auth/login`    | POST   | Login and generate JWT token         |
| `/api/auth/logout`   | POST   | Logout and invalidate JWT token      |

### **Crop Prediction & Management**
| Endpoint          | Method | Description                          |
|-------------------|--------|--------------------------------------|
| `/api/predict`    | POST   | AI-based crop prediction model       |
| `/api/crops`      | GET    | Fetch available crops                |
| `/api/crops/add`  | POST   | Add a new crop listing (for farmers) |
| `/api/crops/:id`  | GET    | Fetch details of a specific crop     |
| `/api/crops/:id`  | PUT    | Update a crop listing                |
| `/api/crops/:id`  | DELETE | Delete a crop listing                |

### **Marketplace**
| Endpoint          | Method | Description                          |
|-------------------|--------|--------------------------------------|
| `/api/market`     | GET    | Get market price trends              |
| `/api/market/buy` | POST   | Place an order for crops             |
| `/api/market/orders` | GET | Fetch all orders for a user          |
| `/api/market/orders/:id` | GET | Fetch details of a specific order    |

### **Shop for Farmers**
| Endpoint          | Method | Description                          |
|-------------------|--------|--------------------------------------|
| `/api/products`   | GET    | Fetch farming products               |
| `/api/products/:id` | GET  | Fetch details of a specific product  |
| `/api/products/add` | POST | Add a new product to the shop        |
| `/api/products/:id` | PUT  | Update a product listing             |
| `/api/products/:id` | DELETE | Delete a product listing            |

### **Cart**
| Endpoint          | Method | Description                          |
|-------------------|--------|--------------------------------------|
| `/api/cart`       | GET    | Fetch cart items for a user          |
| `/api/cart/add`   | POST   | Add an item to the cart              |
| `/api/cart/:id`   | DELETE | Remove an item from the cart         |
| `/api/cart/checkout` | POST | Checkout and place an order         |

### **Voice Assistant**
| Endpoint          | Method | Description                          |
|-------------------|--------|--------------------------------------|
| `/api/voice`      | POST   | Process voice queries (NLP)          |

### **Dashboard & Analytics**
| Endpoint          | Method | Description                          |
|-------------------|--------|--------------------------------------|
| `/api/dashboard`  | GET    | Fetch dashboard data (crop analysis, tasks, etc.) |
| `/api/analytics`  | GET    | Fetch market insights and trends     |

### **User Management**
| Endpoint          | Method | Description                          |
|-------------------|--------|--------------------------------------|
| `/api/users`      | GET    | Fetch all users (admin only)         |
| `/api/users/:id`  | GET    | Fetch details of a specific user     |
| `/api/users/:id`  | PUT    | Update user profile                  |
| `/api/users/:id`  | DELETE | Delete a user (admin only)           |

---

## 📸 Screenshots
![Farmer Home](./assets/farmer_home.png)
![Buyer Home](./assets/buyer_home.png)
![Crop Prediction](./assets/crop_prediction.png)
![Marketplace](./assets/marketplace.png)
![Dashboard](./assets/dashboard.png)

---

## 🤝 Contributors
👤 **Your Name**  
GitHub: [yourusername](https://github.com/yourusername)  
Email: your.email@example.com  

👤 **Contributor 2**  
GitHub: [contributor2](https://github.com/contributor2)  

---

## 📌 Future Improvements
🔹 **Mobile App**: Develop a cross-platform mobile app for better accessibility.  
🔹 **Blockchain Integration**: Ensure transparent and secure transactions.  
🔹 **IoT Integration**: Connect with soil sensors and weather stations for real-time data.  
🔹 **Multi-Language Support**: Add support for regional languages.  
🔹 **Pest Detection**: Use image recognition to detect pests and diseases.  

---

## 📜 License
This project is licensed under the [MIT License](./LICENSE).

---

## 🤝 How to Contribute
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeatureName`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeatureName`).
5. Open a pull request.

---

## 🙏 Acknowledgments
- [OpenWeatherMap API](https://openweathermap.org/) for weather data.
- [TensorFlow](https://www.tensorflow.org/) for AI/ML models.
- [React](https://reactjs.org/) for frontend development.
- [TypeScript](https://www.typescriptlang.org/) for type-safe coding.

---

## 📧 Contact
For questions or feedback, reach out to:  
**Your Name**  
Email: your.email@example.com  
LinkedIn: [Your Profile](https://linkedin.com/in/yourprofile)  
GitHub: [yourusername](https://github.com/yourusername)  

---

## 🚀 Live Demo
Check out the live demo of the project: [GoFarm Live Demo](https://gofarmdemo.com)




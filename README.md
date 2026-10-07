💊 Online Medicine Delivery System – MongoDB

📌 Project Overview

The Online Medicine Delivery System is a database-driven application designed to simplify and manage the process of ordering medicines online.

The project uses MongoDB as the primary database to store and manage information related to users, medicines, prescriptions, orders, payments, inventory, and deliveries.

The system demonstrates how a NoSQL database can be used to build an efficient and scalable medicine delivery platform.

---

🎯 Objectives

- Provide an organized system for managing medicines.
- Allow customers to browse available medicines.
- Manage customer and user information.
- Create and track medicine orders.
- Maintain medicine inventory and stock levels.
- Manage prescription-related information.
- Store payment and order details.
- Track delivery status.
- Demonstrate CRUD operations using MongoDB.
- Practice MongoDB database design and querying.

---

🛠️ Technologies Used

- MongoDB – NoSQL Database
- MongoDB Compass – Database visualization and management
- MongoDB Shell (mongosh) – Database operations and queries
- JSON – Data representation
- JavaScript – MongoDB queries and database operations

---

🗄️ Database Collections

The project can contain the following major collections:

👤 Users

Stores customer and user information.

Example fields:

- User ID
- Name
- Email
- Phone
- Address
- Password
- Role

💊 Medicines

Stores information about available medicines.

Example fields:

- Medicine ID
- Medicine Name
- Category
- Manufacturer
- Price
- Stock
- Expiry Date
- Prescription Required

🛒 Orders

Stores customer order information.

Example fields:

- Order ID
- User ID
- Order Date
- Medicines
- Total Amount
- Payment Status
- Order Status

📋 Prescriptions

Stores prescription-related information.

Example fields:

- Prescription ID
- User ID
- Doctor Name
- Prescription Date
- Medicines
- Verification Status

💳 Payments

Stores payment information.

Example fields:

- Payment ID
- Order ID
- User ID
- Payment Method
- Amount
- Payment Status
- Payment Date

🚚 Deliveries

Stores delivery information.

Example fields:

- Delivery ID
- Order ID
- Delivery Address
- Delivery Partner
- Delivery Status
- Estimated Delivery Date
- Delivered Date

📦 Inventory

Manages medicine stock and inventory information.

Example fields:

- Inventory ID
- Medicine ID
- Quantity
- Reorder Level
- Last Updated

---

🔄 System Workflow

Customer
   ↓
Browse Medicines
   ↓
Select Medicine
   ↓
Add to Cart
   ↓
Upload/Verify Prescription (if required)
   ↓
Place Order
   ↓
Payment
   ↓
Order Confirmation
   ↓
Inventory Updated
   ↓
Delivery Assigned
   ↓
Order Delivered

---

⚙️ MongoDB Operations

The project demonstrates important MongoDB operations such as:

Create

db.medicines.insertOne({
    name: "Paracetamol",
    category: "Pain Relief",
    price: 50,
    stock: 100
});

Read

db.medicines.find({
    category: "Pain Relief"
});

Update

db.medicines.updateOne(
    { name: "Paracetamol" },
    { $inc: { stock: -2 } }
);

Delete

db.medicines.deleteOne({
    name: "Paracetamol"
});

---

📊 Key Features

- 👤 User Management
- 💊 Medicine Management
- 🔍 Medicine Search
- 🛒 Shopping Cart & Orders
- 📋 Prescription Management
- 📦 Inventory Management
- 💳 Payment Management
- 🚚 Delivery Tracking
- 📈 Order & Inventory Analysis
- 🔐 Role-Based Management
- ⚡ MongoDB CRUD Operations

---

📁 Project Structure

Online-Medicine-Delivery-System-MongoDB/
│
├── README.md
│
├── database/
│   ├── database_setup.js
│   ├── collections.js
│   └── sample_data.js
│
├── queries/
│   ├── user_queries.js
│   ├── medicine_queries.js
│   ├── order_queries.js
│   ├── prescription_queries.js
│   ├── payment_queries.js
│   └── delivery_queries.js
│
├── data/
│   └── sample_data.json
│
├── screenshots/
│   └── mongodb_compass.png
│
└── documentation/
    └── project_documentation.pdf

---

🧪 Sample MongoDB Queries

Find all available medicines

db.medicines.find({
    stock: { $gt: 0 }
});

Find medicines requiring a prescription

db.medicines.find({
    prescriptionRequired: true
});

Find pending orders

db.orders.find({
    orderStatus: "Pending"
});

Find low-stock medicines

db.medicines.find({
    stock: { $lt: 10 }
});

Calculate total order value

db.orders.aggregate([
    {
        $group: {
            _id: null,
            totalSales: { $sum: "$totalAmount" }
        }
    }
]);

---

📈 Future Enhancements

The project can be further improved by adding:

- 🌐 Web-based user interface
- 📱 Mobile application
- 🔐 Secure authentication
- 💳 Real-time payment gateway
- 📍 Real-time delivery tracking
- 🤖 AI-based medicine recommendations
- 📊 Admin analytics dashboard
- 🔔 Order and delivery notifications
- ☁️ Cloud deployment
- 🔎 Advanced medicine search and filtering

---

🎓 Learning Outcomes

Through this project, I gained practical experience in:

- MongoDB database design
- NoSQL data modeling
- CRUD operations
- MongoDB queries
- Aggregation pipelines
- Collection relationships
- Inventory management
- Order management
- Database optimization
- Data handling using JSON
- MongoDB Compass and MongoDB Shell

---

👨‍💻 Author

Shrishti Sonker 
BCA DS - 26
46 / 1250258440
BBD University, Lucknow

---

⭐ Project Highlights

«A MongoDB-powered Online Medicine Delivery System designed to demonstrate real-world NoSQL database design, CRUD operations, order management, inventory management, prescription handling, and delivery tracking.»

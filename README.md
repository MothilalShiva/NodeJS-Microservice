# Modular Grocery Microservices API System 🛒

## Overview  
This project demonstrates a modular microservices-based architecture for a grocery shopping system using Node.js. It explores how to structure a Node.js backend with separate services, robust routing, and a Dockerized deployment-ready setup. The goal is to understand clean architecture principles while gaining hands-on experience with API gateway patterns and service isolation.

---

## Features 🚀  
- Modular API design for grocery store operations  
- Separate services for users, products, and cart operations  
- RESTful API endpoints with clear separation of concerns  
- Dockerized setup for easy deployment and scalability  
- Basic in-memory storage for API testing  
- Centralized gateway to route requests to corresponding microservices

---

## Technologies Used 🛠️  
- **Node.js** 🟢  
- **Express.js** ⚙️  
- **Docker** 🐳  
- **REST API** 🌐  
- **JavaScript (ES6+)** 💻  
- **GitHub (Version Control)** 🗂️

---

## Installation & Setup 🏗️  

### Clone the Repository  
```bash
git clone https://github.com/MothilalShiva/NodeJS-Microservice.git
cd NodeJS-Microservice
```

### Run with Docker  
Make sure Docker is installed and running on your system.

```bash
docker-compose up --build
```

This will spin up all services defined in the `docker-compose.yml` file.

### Alternatively, Run Locally (Without Docker)  
```bash
# Navigate into each service and install dependencies
cd api-gateway
npm install
node index.js

cd ../user
npm install
node index.js

cd ../product
npm install
node index.js

cd ../cart
npm install
node index.js
```

---

## Usage 📖  
- Access the **API Gateway** at `http://localhost:3000`  
- Example routes:
  - `GET /user` – Retrieve all users  
  - `POST /product` – Add a new product  
  - `GET /cart` – View items in the cart  
- All routes are forwarded through the API gateway to respective services  
- Modify or add more services/modules as needed to extend functionality  

---

## Project Structure 📂  
```
NodeJS-Microservice/
│
├── api-gateway/              # Central API gateway for routing
│   ├── index.js              # Gateway server
│   └── ...                  
│
├── user/                     # User microservice
│   ├── index.js              # Handles user routes
│   └── ...
│
├── product/                  # Product microservice
│   ├── index.js              # Handles product routes
│   └── ...
│
├── cart/                     # Cart microservice
│   ├── index.js              # Handles cart operations
│   └── ...
│
├── docker-compose.yml        # Docker Compose for containerized orchestration
└── README.md                 # Project documentation
```


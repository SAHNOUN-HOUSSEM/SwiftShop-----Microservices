# SwiftShop | E-commerce Microservices

### Overview
SwiftShop is a distributed e-commerce platform developed with a microservices architecture. It offers a smooth and user-friendly shopping experience with independent services that handle specific functionalities, promoting scalability, reliability, and maintainability.

---

## Table of Contents
- [Repositories](#repositories)
- [Technologies Used](#technologies-used)
- [Architecture](#architecture)
- [Microservices Overview](#microservices-overview)
- [Installation and Setup](#installation-and-setup)

---
## Repositories

The SwiftShop project is split into two repositories for better modularity and organization:

- **Backend Repository:** [PPP_E-commerce_microservices_Backend](https://github.com/SAHNOUN-HOUSSEM/PPP_E-commerce_microservices_Backend)  
  Contains the backend services built with Spring Boot, utilizing a microservices architecture with RabbitMQ, Eureka, Docker, and Kubernetes for orchestration and communication.

- **Frontend Repository:** [PPP_E-commerce_microservices_Frontend](https://github.com/SAHNOUN-HOUSSEM/PPP_E-commerce_microservices_Frontend)  
  Contains the frontend application built with React and TypeScript, providing a user-friendly interface for browsing, cart management, and checkout.

---
## Technologies Used
- **Backend:** Spring Boot, Spring Cloud
- **Frontend:** React with TypeScript
- **Message Broker:** RabbitMQ
- **Service Discovery:** Eureka
- **Containerization and Orchestration:** Docker, Kubernetes

---

## Architecture
SwiftShop is built using a microservices architecture that allows each service to be developed, deployed, and scaled independently. Services communicate synchronously for order processing and data consistency, and asynchronously for tasks like user notifications.

Key components of the architecture include:
- **Eureka Server:** Enables service discovery and synchronous communication.
- **API Gateway:** Manages load balancing, user routing, and authentication.
- **RabbitMQ:** Facilitates asynchronous communication for efficient notification handling.

---

## Microservices Overview

### 1. **Eureka Server**
   - Provides service discovery, enabling microservices to locate and communicate with each other dynamically.

### 2. **API Gateway**
   - Acts as a load balancer and a router.
   - Manages access to other services and communicates with the Auth Service for user authentication.

### 3. **Auth Service**
   - Manages user authentication with JWT tokens for secure access.

### 4. **User Service**
   - Handles user profile updates and stores user-related information.

### 5. **Product Service**
   - Manages the product catalog, allowing users to browse, add to cart, and complete purchases.

### 6. **Order Service**
   - Processes customer orders and updates the product inventory in real-time.

### 7. **Notification Service**
   - Listens to events from the Order and Auth services to inform users of order confirmations and updates.

---



## Installation and Setup

### Prerequisites
Ensure that you have the following installed:
- Docker
- Kubernetes
- RabbitMQ
- Eureka
- Java 8+ for Spring Boot services
- Node.js for the frontend

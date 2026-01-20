# Minimal E-Commerce Backend API

## Overview
This project is a minimal e-commerce backend application developed as part of the in-class assignment provided in the HackMD file. The application is built using Spring Boot and MongoDB and exposes REST APIs only. No frontend is implemented. The goal of this project is to demonstrate how a basic online shopping backend works, including products, cart, orders, payments, and webhook handling, using a clean layered architecture.

---

## Tech Stack
- Java (Spring Boot)
- MongoDB
- Maven
- Lombok
- Postman (for API testing)

---

## Architecture
The project follows a layered architecture to maintain clean separation of responsibilities:

Controller → DTO → Service → Repository → MongoDB

This structure improves maintainability, readability, and follows backend best practices as required in the HackMD assignment.

---

## Project Structure
src/main/java/com/example/ecommerce
├── controller
├── dto
├── model
├── repository
├── service
└── webhook


---

## Features Implemented

### Product Management
- Add new products
- View all available products

### Cart Management
- Add products to a user’s cart
- View cart items for a user
- Clear the cart

### Order Management
- Create an order from cart items
- Calculate total order amount
- Clear cart after order creation

### Payment Handling (Mock)
- Simulate payment for an order
- Update order status to PAID after successful payment

### Webhook
- Simulated payment webhook endpoint to represent payment gateway callbacks

---

## DTO Usage
DTOs (Data Transfer Objects) are used to separate API request and response data from database entities. This avoids exposing internal models directly and follows clean architecture principles.

DTOs implemented:
- CreateProductRequest
- AddToCartRequest
- CreateOrderResponse
- PaymentResponse

---

## API Endpoints

### Product APIs
- POST `/api/products` – Create a product
- GET `/api/products` – Get all products

### Cart APIs
- POST `/api/cart/add` – Add product to cart
- GET `/api/cart/{userId}` – View cart
- DELETE `/api/cart/{userId}/clear` – Clear cart

### Order API
- POST `/api/orders/{userId}` – Create order from cart

### Payment API
- POST `/api/payments/{orderId}` – Make payment (mock)

### Webhook API
- POST `/webhook/payment` – Simulated payment webhook

---

## How to Run the Project

1. Install Java (JDK 17 or above).
2. Install and start MongoDB.
3. Open the project in VS Code or IntelliJ.
4. Run the application using:
5. The server will start at: http://localhost:8080


---

## Testing Using Postman
The APIs are tested in the following sequence:
1. Create a product
2. Add product to cart
3. View cart
4. Create order
5. Make payment
6. Trigger webhook endpoint

---

## Demo Video Instructions
The demo video includes:
- Overview of the project structure
- Explanation of models, services, and controllers
- API testing using Postman
- Complete cart → order → payment flow
- Webhook call demonstration

---

## Notes
- Authentication is not implemented as it was not required.
- Payment gateway is mocked for simplicity.
- The implementation strictly follows the HackMD assignment requirements.

---

## Conclusion
This project demonstrates a complete minimal e-commerce backend system using Spring Boot and MongoDB. It covers product handling, cart operations, order creation, mock payment processing, and webhook simulation while following clean backend architecture and best practices.

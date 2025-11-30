# 🛒 E-Commerce Management System

"This was primarily developed as a course project for HSF302."

## 👥 Team Members:
- [Add your team members here]
- Example: Le Quoc Khanh - SE190302

Big regards and thanks to your contributions throughout the project development!

## 📋 Table of Contents
- [About](#about)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [License](#license)

## 🚀 About

> A comprehensive full-stack e-commerce solution for managing products, orders, payments, and user interactions.

**E-Commerce Management System** is an intelligent online shopping platform that connects customers with products. The system provides a seamless experience for browsing products, managing shopping carts, processing orders, secure payment integration, and administrative management.

### Key Highlights
- 🛍️ **Product Management** - Complete CRUD operations for products with image upload support
- 🛒 **Shopping Cart** - Session-based shopping cart functionality
- 💳 **Secure Payment Processing** - Integrated VNPay payment gateway
- 📊 **Order Management** - Comprehensive order tracking and management system
- 👥 **Multi-role Access** - Separate dashboards for customers, staff, and administrators
- 🔐 **Spring Security** - Secure authentication and authorization
- 📱 **Responsive Design** - Thymeleaf templates with modern UI

## ✨ Features

### For Customers
- User registration and profile management
- Product browsing with advanced filtering and search
- Product detail viewing with multiple images
- Shopping cart management
- Order placement and tracking
- Order history and analytics
- Secure payment processing via VNPay
- Profile editing with address management

### For Staff
- Staff authentication and authorization
- Order management and processing
- Order item editing capabilities
- Payment processing and verification
- Order statistics and reporting

### For Administrators
- Complete system overview dashboard
- Product management (Create, Read, Update, Delete)
- User and customer management
- Order management and monitoring
- System-wide analytics and reporting
- Payment statistics and tracking
- User list management

## 🛠️ Technology Stack

### Backend
- **Framework**: Spring Boot 3.5.6
- **Language**: Java 17
- **Build Tool**: Maven
- **Security**: Spring Security 6
- **Database**: SQL Server with JPA/Hibernate
- **Template Engine**: Thymeleaf
- **Validation**: Spring Validation
- **API**: RESTful endpoints
- **Payment Gateway**: VNPay integration

### Frontend
- **Template Engine**: Thymeleaf (Server-side rendering)
- **Styling**: CSS with custom theme
- **JavaScript**: Vanilla JS (as needed)
- **Static Resources**: Spring Boot static resource handling

## 🚦 Getting Started

### Prerequisites
Ensure you have the following installed:
- **JDK 17** or higher
- **Maven 3.8+**
- **SQL Server** (or SQL Server Express)
- **Git**

### Backend Setup

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd 251007_HSF302_Assignment/demo
   ```

2. **Configure application properties**
   ```bash
   # Edit src/main/resources/application.properties
   # Set your database connection, VNPay credentials, etc.
   ```
   
   Update the following in `application.properties`:
   ```properties
   # Database configuration
   spring.datasource.url=jdbc:sqlserver://localhost:1433;databaseName=HSF302_ASSIGNMENT
   spring.datasource.username=your_username
   spring.datasource.password=your_password
   
   # VNPay configuration
   vnpay.tmnCode=your_tmn_code
   vnpay.hashSecret=your_hash_secret
   vnpay.url=https://sandbox.vnpayment.vn/paymentv2/vpcpay.html
   vnpay.returnUrl=http://localhost:8080/payments/vnpay/return
   ```

3. **Create the database**
   ```sql
   CREATE DATABASE HSF302_ASSIGNMENT;
   ```

4. **Build the project**
   ```bash
   mvn clean install
   ```

5. **Run the application**
   ```bash
   mvn spring-boot:run
   ```
   
   The application will start on `http://localhost:8080` (default)

6. **Access the application**
   - Home page: `http://localhost:8080/`
   - Login: `http://localhost:8080/auth/login`
   - Register: `http://localhost:8080/auth/register`

## 📁 Project Structure

```
251007_HSF302_Assignment/
│
├── demo/                          # Main Spring Boot application
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/example/demo/
│   │   │   │       ├── config/           # Configuration classes
│   │   │   │       │   ├── DataInitializer.java
│   │   │   │       │   ├── SecurityConfig.java
│   │   │   │       │   ├── VnpayConfig.java
│   │   │   │       │   └── WebConfig.java
│   │   │   │       ├── controller/       # REST and MVC controllers
│   │   │   │       │   ├── AuthenticationController.java
│   │   │   │       │   ├── CartController.java
│   │   │   │       │   ├── HomeController.java
│   │   │   │       │   ├── OrderController.java
│   │   │   │       │   ├── PaymentController.java
│   │   │   │       │   ├── ProductController.java
│   │   │   │       │   └── UserController.java
│   │   │   │       ├── model/
│   │   │   │       │   ├── dto/          # Data Transfer Objects
│   │   │   │       │   ├── entity/       # JPA entities
│   │   │   │       │   ├── mapper/       # Entity-DTO mappers
│   │   │   │       │   └── specification/ # JPA specifications
│   │   │   │       ├── repo/             # Repository interfaces
│   │   │   │       ├── service/          # Business logic services
│   │   │   │       └── DemoApplication.java
│   │   │   └── resources/
│   │   │       ├── application.properties
│   │   │       ├── static/               # Static resources (CSS, JS, images)
│   │   │       └── templates/            # Thymeleaf templates
│   │   │           ├── auth/             # Authentication pages
│   │   │           ├── cart/             # Shopping cart pages
│   │   │           ├── layout/           # Layout templates
│   │   │           ├── orders/           # Order management pages
│   │   │           ├── products/         # Product pages
│   │   │           └── user/             # User management pages
│   │   └── test/                         # Unit and integration tests
│   ├── pom.xml                          # Maven configuration
│   └── mvnw                             # Maven wrapper
│
├── uploads/                            # Uploaded product images
└── README.md                            # This file
```

### Code Standards
- Follow existing code style and conventions
- Write meaningful commit messages
- Add comments for complex logic
- Update documentation as needed
- Ensure all tests pass before submitting PR
- Use Lombok annotations for boilerplate code reduction
- Follow Spring Boot best practices

## 🔑 Default Roles

The system supports three user roles:
- **CUSTOMER**: Regular users who can browse, purchase, and manage their orders
- **STAFF**: Staff members who can manage orders and process payments
- **ADMIN**: Administrators with full system access

## 💳 Payment Integration

The system integrates with VNPay payment gateway:
- Sandbox environment for testing
- Secure payment processing
- Payment callback handling
- Payment status tracking

## 📄 License

This project is part of HSF302 course. All rights reserved.

---


# 🍽️ Hotel + Restaurant Management System

<div align="center">

### Enterprise-Grade Microservices Platform for Modern Restaurant & Hotel Operations

Built with **Java Spring Boot**, **ReactJS**, **Oracle Database**, and **Event-Driven Microservices Architecture**.

![Java](https://img.shields.io/badge/Java-17-orange)
![Spring Boot](https://img.shields.io/badge/SpringBoot-Microservices-brightgreen)
![React](https://img.shields.io/badge/Frontend-React-blue)
![Oracle | Postgres](https://img.shields.io/badge/Database-Oracle-red)
![Architecture](https://img.shields.io/badge/Architecture-Microservices-purple)
![Messaging](https://img.shields.io/badge/Messaging-Kafka%20%7C%20RabbitMQ-yellow)

</div>

---

# 📖 Overview

The **Hotel + Restaurant Management System** is a scalable enterprise-grade platform designed to manage restaurant and hotel operations using a **Microservices Architecture**.

The system handles:

- 🍽 Restaurant dine-in & online ordering
- 👨‍🍳 Real-time Kitchen Display System (KDS)
- 📦 Inventory & stock management
- 💳 Billing & payment processing
- 📊 Business analytics & reporting
- 👥 Staff authentication & role management
- 🏨 Future hotel management expansion

The architecture is designed with:

- Event-Driven Communication
- Saga Pattern
- API Gateway Pattern
- Service Discovery
- Maker-Checker Workflow
- Soft Delete & Audit Logging

---

# 🚀 Tech Stack

## 🖥 Frontend

- ReactJS
- Redux Toolkit _(planned)_
- Axios
- React Router
- Material UI / Tailwind _(optional)_

---

## ⚙ Backend

- Java 17
- Spring Boot
- Spring Cloud
- Spring Data JPA
- Hibernate
- Spring Security
- JWT Authentication

---

## 🗄 Database

- Oracle Database

---

## ☁ Infrastructure

- Eureka Service Registry
- Spring Cloud Gateway
- Kafka / RabbitMQ
- Maven Multi-Module Architecture

---

## 🔮 Future Enhancements

- Docker
- Kubernetes
- Redis Cache
- WebSockets
- ELK Stack
- CI/CD Pipelines
- Cloud Deployment

---

# 🏗 System Architecture

```text
                    Frontend (React)
                             |
                             v
                      API Gateway
                             |
                      Eureka Registry
                             |
 -----------------------------------------------------------------
 |         |          |          |          |                    |
 v         v          v          v          v                    v
User     Menu      Order      Kitchen    Billing             Inventory
Service  Service   Service    Service    Service              Service
                              |
                              |
                           Report
                           Service
```

---

# 📦 Microservices

| Service                            | Responsibility                    |
| ---------------------------------- | --------------------------------- |
| 🔐 User Service                    | Authentication & staff management |
| 🍽 Menu Service                    | Menu items & recipe management    |
| 🧾 Order Service                   | Order lifecycle management        |
| 👨‍🍳 Kitchen Service                 | Kitchen Display System workflow   |
| 📦 Inventory Service               | Stock & expense management        |
| 💳 Billing Service                 | Bills, invoices & payments        |
| 📊 Report Service                  | Analytics & reporting             |
| 🌐 API Gateway                     | Centralized API routing           |
| 🛰 Eureka Registry                 | Service discovery                 |
| 🔔 Notification Service _(future)_ | Alerts & notifications            |

---

# ✨ Core Features

## 🍽 Restaurant Operations

- Dine-in ordering
- Online ordering
- Table session management
- Incremental ordering support
- Order lifecycle tracking

---

## 👨‍🍳 Kitchen Display System (KDS)

Real-time kitchen workflow dashboard.

### Order States

```text
NEW
PREPARING
READY
DELIVERED
```

### Features

- Live kitchen queue
- Cook assignment
- Preparation tracking
- Delay highlighting
- Real-time order updates

---

## 📦 Inventory Management

- Ingredient management
- Daily stock entry
- Stock usage tracking
- Kitchen expense management
- Stock movement history

### Maker-Checker Workflow

Implemented for:

- Stock Entries
- Kitchen Expenses

Approval States:

```text
PENDING
APPROVED
REJECTED
```

---

## 💳 Billing & Payments

- Bill generation
- Tax/GST calculation
- Invoice generation
- Payment processing

### Supported Payment Methods

```text
CASH
CARD
UPI
ONLINE
```

---

## 📊 Reporting & Analytics

Generate:

- Daily Reports
- Monthly Reports
- Yearly Reports
- Item Sales Analytics
- Revenue & Expense Reports
- Profit Analytics

---

# 🔄 Event-Driven Architecture

Services communicate asynchronously using:

- Kafka
  OR
- RabbitMQ

## 📡 Main Domain Events

```text
ORDER_CREATED
ORDER_PREPARING
ORDER_READY
ORDER_SERVED
PAYMENT_COMPLETED
STOCK_UPDATED
EXPENSE_APPROVED
ORDER_CANCELLED
```

---

# 🧠 Enterprise Architecture Patterns

## ✅ Microservices Architecture

Each service:

- owns its own database schema
- has independent business logic
- can be deployed independently

---

## ✅ Saga Pattern

Used for distributed transaction consistency.

### Example

If inventory deduction fails:

```text
Cancel Order
Remove Kitchen Order
Cancel Draft Bill
```

---

## ✅ Soft Delete Strategy

Important entities use:

```text
is_deleted
```

instead of physical deletion.

---

## ✅ Audit Logging

Most entities contain:

```text
created_by
created_at
updated_by
updated_at
```

---

# 🗄 Database Design Overview

## 🧾 Order Service

- restaurant_tables
- table_sessions
- orders
- order_items
- order_status_history

---

## 👨‍🍳 Kitchen Service

- kitchen_orders
- kitchen_order_items
- kitchen_order_history

---

## 📦 Inventory Service

- ingredients
- stock_entries
- stock_usage
- kitchen_expenses
- stock_transaction_history

---

## 💳 Billing Service

- bills
- bill_items
- payments
- invoices

---

## 🔐 User Service

- roles
- staff_users
- user_sessions
- user_activity_logs

---

## 📊 Report Service

- daily_sales_reports
- monthly_sales_reports
- yearly_sales_reports
- item_sales_reports

---

# 📂 Project Structure

```text
restaurant-system
│
├── common-module
│
├── service-registry
├── api-gateway
│
├── user-service
├── menu-service
├── order-service
├── kitchen-service
├── inventory-service
├── billing-service
├── report-service
│
└── frontend-react
```

---

# 🔐 Authentication & Security

- JWT Authentication
- Role-Based Access Control (RBAC)
- Gateway-level token validation

## 👥 Roles

```text
ADMIN
WAITER
COOK
COUNTER
INVENTORY
```

---

# 🌐 API Gateway Routes

```text
/api/users
/api/menu
/api/orders
/api/kitchen
/api/inventory
/api/billing
/api/reports
```

---

# ⚡ Development Roadmap

## Phase 1 — Infrastructure

- Eureka Service Registry
- API Gateway
- common-module

---

## Phase 2 — Authentication

- User Service

---

## Phase 3 — Core Restaurant Operations

- Menu Service
- Order Service
- Kitchen Service

---

## Phase 4 — Inventory & Billing

- Inventory Service
- Billing Service

---

## Phase 5 — Reporting & Analytics

- Report Service

---

## Phase 6 — Event Integration

- Kafka / RabbitMQ
- Saga Pattern

---

# 🛠 Backend Standards

## Recommended Package Structure

```text
controller
service
repository
entity
dto
config
exception
producer
consumer
```

---

## Naming Conventions

### Database

- snake_case

### Java

- PascalCase → Classes
- camelCase → Variables

---

# 📈 Future Enhancements

## 🏨 Hotel Management Expansion

- Room Booking
- Housekeeping
- Guest Management
- Room Service
- Hotel Billing

---

## ☁ Scalability Enhancements

- Multi-Branch Support
- Redis Cache
- WebSockets
- Docker Deployment
- Kubernetes Orchestration
- Cloud Infrastructure

---

## 🤖 AI & Analytics

- Sales Forecasting
- Demand Prediction
- Inventory Forecasting
- Recommendation Engine

---

# 👨‍💻 Author

## Adwyait Pawar

Associate Software Developer

Java • Spring Boot • Microservices • React • Oracle DB

## Anand Lande

Salesforce Developer Trainee

Java • Spring Boot • Microservices • React • Apex • LWC • Flows • Postgres DB

---

# ⭐ Vision

To build a modern enterprise-grade platform capable of supporting:

- Restaurant Operations
- Hotel Operations
- Inventory Management
- Real-Time Kitchen Workflow
- Billing & Payments
- Reporting & Analytics
- Cloud-Ready Deployment

---

<div align="center">

### 🚀 Building scalable hospitality systems with Microservices Architecture.

</div>

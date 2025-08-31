# E-Bike Rental Platform

## Overview

This project is a **microservices-based e-bike rental platform** designed to provide a seamless bike-sharing experience. It enables users to register, authenticate, book rides, make payments, receive notifications, earn rewards, and leave reviews.

The system follows a **scalable event-driven architecture** with services communicating via a **message broker** for reliability and loose coupling.

---

## Features

* Authentication and User Management – Secure login, registration, and user profiles.
* Bike and Ride Management – View available bikes, reserve rides, and track ride details.
* Payments Integration – Integrated with Stripe for secure transactions.
* Notifications – Real-time updates for bookings, payments, and ride events.
* Rewards System – Earn points for rides and redeem rewards.
* Reviews – Share feedback and rate rides.

---

## System Architecture

[View on Eraser![](https://app.eraser.io/workspace/ZZuUR9TQXhSrp0EduFAK/preview?elements=b_Zk5mil_KBPsS5rQaMnRA\&type=embed)](https://app.eraser.io/workspace/ZZuUR9TQXhSrp0EduFAK?elements=b_Zk5mil_KBPsS5rQaMnRA)

---

### Components

* **Frontend**: React (user interface)
* **API Gateway**: Nginx (routing requests to microservices)
* **Microservices**:

  * Auth Service (PostgreSQL)
  * User Service (PostgreSQL)
  * Bike Service (PostgreSQL)
  * Ride Service (PostgreSQL)
  * Payment Service (MongoDB + Stripe)
  * Notification Service (MongoDB)
  * Reward Service (MongoDB)
  * Review Service (PostgreSQL)
* **Message Broker**: Apache Kafka

  * Ride Events Topic
  * Payment Events Topic

Each service has its own database for data isolation and scalability.

---

## Tech Stack

* **Frontend**: React
* **Gateway**: Nginx
* **Backend Services**: Ballerina (per service)
* **Databases**: PostgreSQL and MongoDB
* **Event Streaming**: Apache Kafka
* **Payments**: Stripe

---

## Getting Started

### Prerequisites

* Docker and Docker Compose
* Node.js (v18 or higher)
* PostgreSQL and MongoDB
* Kafka

### Setup

```bash
# Clone repository
git clone https://github.com/thetharz/ebike-rental-platform.git
cd ebike-rental-platform

# Start services
docker compose up -d
```

---

## Communication Flow

1. The frontend communicates with services via the API Gateway.
2. Each microservice manages its own domain logic and data.
3. Kafka handles ride and payment events for asynchronous communication.
4. Stripe is used for secure payment processing.

---

## Collaborators

* **Tharindu Imalka** 
* **Tharindu Geethanjan** 
* **Dulshan Siriwardhana** 
* **Sahan Gawesh** 

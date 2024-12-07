# Software Design Description (SDD)

## 1. Introduction

### 1.1 Purpose
The purpose of this Software Design Description (SDD) is to provide a detailed design for the Uber ride-hailing application. This document describes the software's architecture, components, interfaces, and their interactions to ensure that the implementation meets the system's functional and non-functional requirements.

### 1.2 Scope
The Uber system enables riders to request and pay for rides via a mobile app. Drivers are able to offer services through the same platform. The system includes the mobile application, backend API services, payment processing, real-time communication, and external integration with services like maps and SMS gateways.

## 2. System Overview

The Uber system is composed of three main modules:

- **Mobile Application** (UI for both riders and drivers)
- **Backend System** (API and Business Logic)
- **External Services** (Third-party integrations like Payment Gateway, Maps API, SMS Gateway)

The system operates across Android and iOS devices and communicates with a backend through REST APIs. The backend uses a cloud-hosted, scalable architecture for high availability and performance.

## 3 Architecture Design

### 3.1 Architecture Components

#### User Interfaces
- **Rider App**
  - Registration/Login
  - Ride Booking (Pickup & Drop-off)
  - Real-time Ride Tracking
  - Payment Gateway Integration
  - Trip History & Ratings

- **Driver App**
  - Registration/Login with KYC
  - Accept/Reject Ride Requests
  - Navigation to Pickup & Drop-off
  - Earnings Dashboard

- **Admin Dashboard**
  - User Management (Drivers & Riders)
  - Ride Monitoring
  - Analytics and Reporting

---

### 3.2 Backend Services
- **Authentication**  
  Secure login and token-based rider/driver authentication (JWT).  

- **Ride Management**  
  Matching riders with drivers, tracking ride lifecycle, and calculating fares.  

- **Real-time Communication**  
  WebSocket-based real-time updates for ride status and driver location.  

- **Payment Integration**  
  Processing payments, refunds, and tips via gateways like Stripe or Razorpay.  

---

### 3.3 Databases
- **PostgreSQL**  
  Storing structured data (rider/driver profiles, rides, payments).  

- **Redis**  
  Caching real-time data (driver locations, active rides).  

---

### 3.4 External APIs
- **Google Maps API**  
  Location services for geocoding, distance calculation, and routing.  

- **Payment Gateway (Stripe)**  
  For secure online payments and refunds.  

---

### 3.5 Infrastructure
- **Hosting**  
  Cloud services like AWS or Google Cloud for backend and databases.  

- **Load Balancer**  
  Nginx or AWS ELB for traffic distribution.  

- **Monitoring Tools**  
  Prometheus and Grafana for performance metrics and logging.  

- **CI/CD Pipeline**  
  Automated deployments using GitHub Actions or Jenkins.  

---

## 3.6 Workflow Overview
1. **Rider books a ride**
   - Inputs pickup and drop-off locations.
   - Backend matches the request with an available driver.

2. **Driver accepts/rejects the ride**
   - Real-time updates sent to the rider.

3. **Ride starts and completes**
   - Driver and rider locations are tracked.
   - Notifications sent at each stage.

4. **Payment processed**
   - Automatically via the app.

5. **Admin oversight**
   - Admin dashboard displays live analytics and operational metrics.

## 4. Module Design

### 4.1 Mobile Application (Frontend)

#### 4.1.1 User Interface (UI)
The UI is designed to be simple, responsive, and easy to use. The UI components include:
- Home Screen
- Ride Booking Screen
- Ride Status
- Payment Screen
- Profile Management

#### 4.1.2 Controller Layer
Manages rider/driver requests and communicates with the service layer for processing. This includes:
- Ride Booking Controller
- Authentication Controller
- Payment Controller

#### 4.1.3 Service Layer
Handles business logic like ride requests, payment processing, and notifications.

### 4.2 Backend System (Server-side)

#### 4.2.1 API Gateway
The API Gateway serves as the entry point for all mobile application requests. It forwards requests to appropriate backend services.

#### 4.2.2 Authentication Service
Handles:
- Rider/Driver registration
- Rider/Driver login
- Password recovery and reset

#### 4.2.3 Ride Management Service
Handles:
- **Ride Creation**: Riders create ride requests with pickup and drop-off locations.
- **Fare Calculation**: Fare is calculated based on distance and time.
- **Ride Matching**: Matches riders with drivers based on proximity.

#### 4.2.4 Payment Service
Manages:
- Payment processing using external payment gateways.
- Maintaining payment history for riders.

#### 4.2.5 Notification Service
Responsible for sending notifications to riders and drivers about ride status changes.

## 5. Database Design
The Uber system uses a NoSQL database (e.g., MongoDB). Below is the database schema for major entities. 

![Design](https://github.com/user-attachments/assets/2e0649d3-c90b-45fa-96b2-26930fb27858)

### Explanation:
- **Users**: Stores rider/driver details like name, contact, preferences.
- **Drivers**: Stores details about drivers, including their vehicle information and ratings.
- **Rides**: Stores ride-related information like pickup, drop-off, and status.
- **Payments**: Stores payment transaction details.

## 6. Interface Design

### 6.1 API Design
Below are some of the REST API endpoints for interaction:

![API Endpoints](https://github.com/user-attachments/assets/7ce242c4-adf0-4954-a18f-e66782a6dacb)

### 6.2 External System Interfaces
- **Payment Gateway**: Handles payment transactions (e.g., Stripe, PayPal).
- **Maps API**: Provides geolocation and mapping services.
- **SMS Gateway**: Sends notifications to riders and drivers (e.g., Twilio).

### 6.3 Notification Flow Diagram
This diagram represents the flow of notifications between services.

## 7. Non-Functional Requirements

![Design](https://github.com/user-attachments/assets/7fc22453-68b7-4634-8b21-4158d7976f6c)

### 7.1 Performance
The system should handle at least 10,000 simultaneous users.

### 7.2 Scalability
The backend must be horizontally scalable.

### 7.3 Availability
99.9% uptime with redundancy in critical components.

### 7.4 Security
Data encryption for sensitive information.

## 8. Conclusion
This Software Design Description outlines the architecture, modules, database, and interfaces for the Uber system, ensuring the application is robust, scalable, and secure. The use of modular design and external system integration ensures that the system is capable of handling a large number of riders and drivers effectively.

## Chatgpt prompt
Create a Software Design Description (SDD) outline for a platform that connects service providers with customers.


# Software Design Description (SDD)

## 1. Introduction

### 1.1 Purpose
The purpose of this Software Design Description (SDD) is to provide a detailed design for the Uber clone ride-hailing application. This document describes the software's architecture, components, interfaces, and their interactions to ensure that the implementation meets the system's functional and non-functional requirements.

### 1.2 Scope
The Uber clone system enables users to request and pay for rides via a mobile app. Drivers are able to offer services through the same platform. The system includes the mobile application, backend API services, payment processing, real-time communication, and external integration with services like maps and SMS gateways.

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
Manages user requests and communicates with the service layer for processing. This includes:
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
- User registration
- User login
- Password recovery and reset

#### 4.2.3 Ride Management Service
Handles:
- **Ride Creation**: Users create ride requests with pickup and drop-off locations.
- **Fare Calculation**: Fare is calculated based on distance and time.
- **Ride Matching**: Matches users with drivers based on proximity.


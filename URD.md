# User Requirements Document (URD)

## 1. Introduction

### 1.1 Purpose
This document outlines the user requirements for the Uber application. It is intended to guide the design, development, and testing of the application to ensure that it meets the needs of its users, including riders and drivers.

### 1.2 Scope
Uber will be a ride-hailing mobile application that connects riders with drivers. The app will support booking rides, real-time tracking, payment processing, and communication between riders and drivers.

### 1.3 Definitions, Acronyms, and Abbreviations
- **Rider/User**: An individual who uses the app to book a ride.
- **Driver**: An individual who uses the app to offer ride services.
- **Admin**: The entity responsible for managing and overseeing the app’s operations.
- **ETA**: Estimated Time of Arrival.

### 1.4 References
- [Stakeholders.md](https://github.com/IIITLucknowSWEngg/CSAICSBTeam002/blob/main/stakeholders.md)
- [Project.md](https://github.com/IIITLucknowSWEngg/CSAICSBTeam002/blob/main/Project.md)

---

## 2. User Characteristics

### 2.1 Riders
- Typically smartphone users familiar with basic app navigation.
- Expect a seamless and quick ride-booking experience.
- Value real-time updates, transparent pricing, and safety features.

### 2.2 Drivers
- Smartphone users who need clear, easy-to-follow instructions for accepting and completing rides.
- Prefer intuitive interfaces for managing ride requests and navigation.
- Require clear payment details and history tracking.

---

## 3. Functional Requirements

### 3.1 User Registration and Login
**Riders and Drivers:**
- Must be able to register using an email address or phone number.
- Must be able to log in using their credentials.
- Password reset functionality should be available.

### 3.2 User Profiles
**Riders:**
- Must be able to create and edit their profile, including contact information and payment methods.
- Must be able to view their ride history and payment history.

**Drivers:**
- Must be able to create and edit their profile, including vehicle information and availability.
- Must be able to view their ride history, earnings, and ratings.

### 3.3 Ride Booking and Management
**Riders:**
- Must be able to enter a pickup and drop-off location.
- Must be able to view available drivers nearby and their estimated arrival time.
- Must receive a fare estimate before confirming the ride.
- Must be able to cancel a ride before it starts.
- Must receive notifications about the driver’s arrival, ride start, and ride completion.

**Drivers:**
- Must receive ride requests with details of the pickup location and rider information.
- Must be able to accept or decline ride requests.
- Must be able to use in-app navigation to reach the pickup and drop-off locations.
- Must receive notifications for ride cancellations or changes.

### 3.4 Payment Processing
**Riders:**
- Must be able to choose from multiple payment methods (credit/debit card, in-app wallet).
- Must receive a payment confirmation after the ride is completed.
- Must be able to view payment history.

**Drivers:**
- Must be able to track earnings from completed rides.
- Must receive payment directly to their chosen payout method.

### 3.5 Ratings and Reviews
**Riders:**
- Must be able to rate and review drivers after each ride.

**Drivers:**
- Must be able to rate and review riders after each ride.

### 3.6 Communication
**Riders and Drivers:**
- Must be able to communicate via in-app chat or call for coordination.
- Notifications should be sent for messages received.

### 3.7 Real-Time Tracking
**Riders:**
- Must be able to track the driver’s location in real-time after booking the ride.

**Drivers:**
- Must be able to view the rider’s location for pickup.

### 3.8 Customer Support
**Riders and Drivers:**
- Must be able to access customer support through the app.
- FAQs and help sections should be easily accessible.

### 3.9 Admin Panel
**Admins:**
- Must be able to manage users (approve, suspend, or delete accounts).
- Must be able to view real-time data on active rides.
- Must be able to access ride and payment history for all users.

---

## 4. Non-Functional Requirements

### 4.1 Performance
- The app must load within 2 seconds under normal network conditions.
- Ride requests, driver acceptances, and status updates must be processed and displayed to all relevant parties (users and drivers) within 1 second, ensuring real-time synchronization and minimal latency.

### **4.2 Security**

- **Data Encryption**:  
  All user data must be encrypted using **AES-256** for data at rest and **TLS 1.3** for data in transit to protect against unauthorized access.

- **Regulatory Compliance**:  
  The app must adhere to data protection regulations applicable in India, such as:  
  - **Personal Data Protection Bill (PDPB)** or its successor laws by implementing:  
    - Explicit user consent for data collection and usage.  
    - Rights for users to access, modify, and delete their personal data.  
    - Data anonymization to ensure privacy.  
  - Compliance with **IT Act, 2000**, ensuring:  
    - Secure handling of sensitive personal information.  
    - Protection against unauthorized access, data breaches, and misuse.  


- **User Authentication**:  
  Authentication must include:  
  - Secure password policies (minimum 8 characters, including uppercase, lowercase, numbers, and symbols).  
  - Multi-factor authentication (e.g., OTP via SMS or email, or authenticator apps).

- **Access Control**:  
  Implement **Role-Based Access Control (RBAC)** to restrict access to sensitive features or data based on user roles.


### **4.3 Usability**

- **Intuitive Design**:  
  The app must have a clear, user-friendly interface with minimal learning curve, ensuring:  
  - Riders can book rides, and drivers can accept requests within three taps or fewer.

- **Navigation**:  
  Logical workflows and clearly labeled buttons/icons must guide users through tasks such as:  
  - Ride booking, accepting requests, and payment completion without confusion.

- **Responsive UI**:  
  The app must maintain full functionality and visual consistency on devices with screen sizes ranging from **4 inches to 10 inches** (smartphones and tablets).

- **Accessibility**:  
  The app must comply with **WCAG 2.1 Level AA** standards, including:  
  - High-contrast text and color schemes.  
  - Support for screen readers.  
  - Adjustable font sizes.  
  - Touch-friendly buttons with a minimum size of **48x48 pixels**.


### 4.4 Reliability
- The app must be available 99.9% of the time, with minimal downtime.
- Backup systems should ensure data is not lost in case of server failure.

### **4.5 Scalability**

- **Performance Under Load**:  
  The app must handle up to **10,000 concurrent users** initially and scale to support **100,000 concurrent users** within 12 months without degradation in performance (e.g., maintaining response times under 2 seconds).

- **Elastic Infrastructure**:  
  The backend must leverage scalable cloud infrastructure (e.g., AWS, Azure, or Google Cloud) to dynamically allocate resources based on user demand, ensuring cost-efficiency and high availability.

- **Modular Architecture**:  
  The backend must be designed with a **microservices architecture**, enabling the independent deployment and scaling of services (e.g., authentication, ride management, payment processing).

- **Support for New Features**:  
  The system must support the seamless addition of new features or updates (e.g., ride-sharing, multi-stop rides) without requiring significant rework to existing components or downtime.

- **Database Scalability**:  
  The database must support horizontal scaling, allowing for efficient handling of increased data volume and ensuring consistency and reliability through techniques like sharding and replication.


---

## 5. Assumptions and Dependencies
- The app will rely on third-party services for map integration, payment processing, and notifications.
- The project assumes that users will have access to smartphones and stable internet connections.

---

## 6. Acceptance Criteria
- The app must pass all functional and non-functional tests.
- User feedback during the beta testing phase must be addressed before the final release.
- The app must meet all security and performance benchmarks outlined in this document.

---

## 7. Conclusion
This document defines the user requirements for the Uber application. It serves as a guide for the development team to ensure that the final product meets the needs of the end-users and aligns with the project’s goals.

## Chatgpt prompt used
Outline a User Requirements Document (URD) for a ride-hailing app, covering key sections .

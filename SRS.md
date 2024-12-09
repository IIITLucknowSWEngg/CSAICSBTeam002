# Software Requirements Specification (SRS) Document

## 1. Introduction

### 1.1 Purpose
This Software Requirements Specification (SRS) document provides a comprehensive overview of the requirements for the Uber application. It includes both functional and non-functional requirements and serves as a guideline for developers, testers, and stakeholders throughout the software development lifecycle.

### 1.2 Scope
The Uber application is a ride-hailing platform that enables drivers and riders to connect via a mobile application. The system will handle user registration, ride booking, payment processing, and driver management. This SRS covers all aspects of the application, including user interfaces, functional and non-functional requirements, and external interface requirements.

### 1.3 Definitions, Acronyms, and Abbreviations
- **SRS**: Software Requirements Specification  
- **NFR**: Non-Functional Requirement  
- **UI**: User Interface  
- **API**: Application Programming Interface  
- **GPS**: Global Positioning System  
- **ETA**: Estimated Time of Arrival  

### 1.4 References
- IEEE Std 830-1998, IEEE Recommended Practice for Software Requirements Specifications  
- SWEBOK v4.0, Software Engineering Body of Knowledge  
- [Stakeholders.md  ](https://github.com/IIITLucknowSWEngg/CSAICSBTeam002/blob/main/stakeholders.md)
- [User Requirements Document](https://github.com/IIITLucknowSWEngg/CSAICSBTeam002/blob/main/URD.md)  

### 1.5 Overview
This document is organized into several sections that describe the overall system, functional requirements, non-functional requirements, and other considerations relevant to the development and implementation of the Uber application.

## 2. Overall Description

### 2.1 Product Perspective
The Uber application is an independent system designed to operate on mobile devices. It interfaces with external systems such as payment gateways, GPS services, and third-party APIs for map integration. The system will be built using a modular architecture to facilitate scalability and maintainability.

### 2.2 Product Functions
- Rider, Driver and Admin registration and authentication.  
- Ride booking and management.  
- Real-time driver tracking.  
- Payment processing and history tracking.  
- Rating and review system.  
- In-app communication between drivers and riders.  

### 2.3 User Classes and Characteristics
- **Riders**: Individuals using the app to book rides.  
- **Drivers**: Individuals using the app to offer ride services.  
- **Admins**: Individuals managing the platform, overseeing driver and rider activities.  

### 2.4 Operating Environment
The application will operate on Android and iOS mobile platforms. It will require internet connectivity for real-time functionalities like ride booking, payment processing, and GPS tracking. The backend will be hosted on cloud servers with high availability and reliability.

### 2.5 Design and Implementation Constraints
- Must comply with data protection regulations (e.g., GDPR).  
- Limited by the performance and capabilities of mobile devices.  
- Dependency on third-party services for payments and GPS tracking.  

### 2.6 Assumptions and Dependencies
- Users have access to smartphones with stable internet connections.  
- Integration with third-party services is stable and reliable.  
- The application will initially support only one currency and language.  

## 3. System Features

### 3.1 User Registration and Authentication
**Description:** Users can register using email or phone numbers. The system supports secure login and password recovery.

**Functional Requirements:**  
- The system shall allow users to register with an email or phone number.  
- The system shall send a verification code to the user for account activation.  
- The system shall support password recovery via email or SMS.  

### 3.2 Ride Booking
**Description:** Riders can book rides by specifying pickup and drop-off locations. The system calculates the fare and provides an ETA.

**Functional Requirements:**  
- The system shall allow riders to enter a pickup and drop-off location.  
- The system shall provide an estimated fare and ETA before confirming the ride.  
- The system shall notify the driver of a new ride request.  

### 3.3 Payment Processing
**Description:** The system processes payments through various methods and records payment history.

**Functional Requirements:**  
- The system shall allow riders to choose a payment method (credit/debit card, in-app wallet).  
- The system shall automatically charge the rider after the ride is completed.  
- The system shall maintain a payment history for riders and drivers.  

### 3.4 Rating and Reviews
**Description:** Riders can rate and review drivers after each ride, and drivers can rate riders.

**Functional Requirements:**  
- The system shall allow riders to rate and review drivers after each ride.  
- The system shall allow drivers to rate riders after each ride.  

## 4. External Interface Requirements

### 4.1 User Interfaces
- **Mobile Application:** The UI will be intuitive, offering easy navigation and access to key functionalities. Designed to be responsive, it will ensure compatibility across various screen sizes.  
- **Admin Panel:** A web-based admin panel that provides a comprehensive dashboard for managing drivers, riders, and rides. It will include analytics and reporting features.  

### 4.2 Hardware Interfaces
The system will interact with mobile device hardware, including:  
- **GPS Modules:** For tracking pickup and drop-off locations.  
- **Cameras:** Used for profile pictures.  
- **NFC:** For mobile payments.  

### 4.3 Software Interfaces
- **Third-Party APIs:** Integration with APIs for payment processing, map services, and SMS notifications.  
- **Database:** The system will use a NoSQL database (e.g., MongoDB) for data storage.  

### 4.4 Communication Interfaces
- The application will communicate over secure HTTPS protocols, ensuring data privacy and integrity.  
- It will use WebSocket for real-time updates and notifications.  

## 5. Non-Functional Requirements (NFRs)

### 5.1 Performance Requirements
- The application shall load within 2 seconds on mobile devices under normal network conditions.  
- The system shall handle up to 10,000 concurrent users without performance degradation.  
- Ride requests shall be processed and matched with drivers within 5 seconds.  

### 5.2 Security Requirements
- User data shall be encrypted both in transit (using TLS) and at rest (using AES-256).  
- The system shall enforce strong password policies, including multi-factor authentication for users.  
- Regular security audits and penetration testing shall be conducted to identify and mitigate vulnerabilities.  

### 5.3 Availability and Reliability
- The system shall achieve 99.9% uptime, with minimal downtime for maintenance.  
- The application shall be resilient to server failures, with automatic failover mechanisms in place.  
- Data backups shall be performed daily and stored in geographically diverse locations.  

### 5.4 Scalability
- The system architecture shall support horizontal scaling to handle increased load.  
- The application shall be designed to accommodate new features and services without significant refactoring.  
- The database shall be optimized to handle large volumes of data, with efficient indexing and query optimization.  

### 5.5 Usability
- The UI/UX design shall prioritize ease of use, ensuring that all users can navigate the application without extensive training.  
- The application shall be accessible to users with disabilities, following WCAG 2.1 guidelines.  
- User feedback mechanisms shall be integrated to continuously improve the usability of the application.  

### 5.6 Maintainability
- The codebase shall be modular, with clear separation of concerns to facilitate easy maintenance and updates.  
- Comprehensive documentation shall be maintained for all system components, including APIs, database schemas, and user interfaces.  
- The system shall support automated testing to ensure that new updates do not introduce regressions.  

### 5.7 Compliance
- The system shall comply with relevant data protection regulations, including GDPR.  
- Payment processing shall adhere to PCI-DSS standards.  
- The system shall include features for user data export and deletion to comply with privacy regulations.  

## 6. Other Requirements
- **Localization:** The application shall support localization to enable use in different regions with minimal changes.  
- **Ethical Requirements:** The application shall include features to prevent misuse, such as reporting mechanisms for inappropriate behavior by drivers or riders.  

## 7. Appendices
- **Appendix A:** Glossary of Terms  
- **Appendix B:** Diagrams (System Architecture, Use Case Diagrams)  
- **Appendix C:** Detailed Requirements Matrix  


# Appendix B: Use Case Diagram
# Happy Path Diagram
Below is the Use Case Diagram for the happy path of the Uber clone application. It illustrates the primary actors (Rider, Driver, and Admin) and their interactions with the system for key processes like User Registration, Ride Booking, Payment Processing, Rating and Reviews, and Admin Management.

![Happy path](https://github.com/user-attachments/assets/835567f6-7cfd-4208-9eef-a3af320e864a)


The diagram details the step-by-step flow for each interaction, representing the standard sequence of actions without any exception handling (happy path):
- Actors:
  - Rider: Registers, books rides, pays, and rates drivers.
  - Driver: Manages availability, accepts rides, completes rides, and rates riders.
  - Admin: Monitors activities, manages users, and accesses analytics.

# Abuse Case Diagram

![Abuse Case Diagram](https://github.com/user-attachments/assets/77b92713-a86a-4e54-97c7-2dabc33c9418)

# Error Case Diagram

<img width="630" alt="error_case" src="https://github.com/user-attachments/assets/c576679c-3c14-4726-bc97-d6941b2d3f87">

## Chatgpt prompt
Create a Software Requirements Specification (SRS) outline for a platform that connects service providers with customers.

# User Requirements Document (URD)

## 1. Introduction

### 1.1 Purpose
This document outlines the user requirements for the Uber clone application. It is intended to guide the design, development, and testing of the application to ensure that it meets the needs of its users, including riders and drivers.

### 1.2 Scope
The Uber clone will be a ride-hailing mobile application that connects riders with drivers. The app will support booking rides, real-time tracking, payment processing, and communication between riders and drivers.

### 1.3 Definitions, Acronyms, and Abbreviations
- **Rider/User**: An individual who uses the app to book a ride.
- **Driver**: An individual who uses the app to offer ride services.
- **Admin**: The entity responsible for managing and overseeing the app’s operations.
- **ETA**: Estimated Time of Arrival.

### 1.4 References
- [Stakeholders.md](https://github.com/IIITLucknowSWEngg/CSAICSBTeam002/blob/main/stakeholders.md)
- [Project.md](https://github.com/IIITLucknowSWEngg/CSAICSBTeam002/blob/main/Project.md)


## 2. User Characteristics

### 2.1 Riders
- Typically smartphone users familiar with basic app navigation.
- Expect a seamless and quick ride-booking experience.
- Value real-time updates, transparent pricing, and safety features.

### 2.2 Drivers
- Smartphone users who need clear, easy-to-follow instructions for accepting and completing rides.
- Prefer intuitive interfaces for managing ride requests and navigation.
- Require clear payment details and history tracking.

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

## 4. Non-Functional Requirements

### 4.1 Performance
- The app must load within 2 seconds under normal network conditions.
- Ride requests and updates must be processed in real-time.

### 4.2 Security
- User data must be encrypted in transit and at rest.
- The app must comply with data protection regulations (e.g., GDPR).
- User authentication must be secure, with options for multi-factor authentication.

### 4.3 Usability
- The app must be intuitive and easy to navigate for both riders and drivers.
- The UI must be responsive and accessible on devices with various screen sizes.

### 4.4 Reliability
- The app must be available 99.9% of the time, with minimal downtime.
- Backup systems should ensure data is not lost in case of server failure.

### 4.5 Scalability
- The app must be able to handle a growing number of users without degradation in performance.
- The backend should support the addition of new features without significant rework.

## 5. Assumptions and Dependencies
- The app will rely on third-party services for map integration, payment processing, and notifications.
- The project assumes that users will have access to smartphones and stable internet connections.

## 6. Acceptance Criteria
- The app must pass all functional and non-functional tests.
- User feedback during the beta testing phase must be addressed before the final release.
- The app must meet all security and performance benchmarks outlined in this document.

## 7. Conclusion
This document defines the user requirements for the Uber clone application. It serves as a guide for the development team to ensure that the final product meets the needs of the end-users and aligns with the project’s goals.



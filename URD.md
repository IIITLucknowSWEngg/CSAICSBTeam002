# User Requirements Document (URD)

## 1. Introduction  

### 1.1 Purpose  
This document outlines my requirements for the Uber application. It will guide the design, development, and testing of the application to ensure that it meets my needs as a user, whether I’m booking rides as a rider or providing rides as a driver.  

### 1.2 Scope  
Uber will be a ride-hailing mobile application connecting me with other users. As a rider, I’ll use it to book rides, track drivers in real-time, and pay seamlessly. As a driver, I’ll use it to manage ride requests and earn income efficiently.  

### 1.3 Definitions, Acronyms, and Abbreviations  
- **Rider/User**: Someone like me who uses the app to book rides.  
- **Driver**: Someone offering rides through the app.  
- **Admin**: The person managing and overseeing the app’s operations.  
- **ETA**: Estimated Time of Arrival.  

### 1.4 References  
- [Stakeholders.md ](https://github.com/IIITLucknowSWEngg/CSAICSBTeam002/blob/main/stakeholders.md) 
- [Project.md  ](https://github.com/IIITLucknowSWEngg/CSAICSBTeam002/blob/main/Project.md)

---

## 2. User Characteristics  

### 2.1 Riders  
As a rider, I’m familiar with basic app navigation on my smartphone. I expect a smooth, quick ride-booking experience with features like real-time updates, transparent pricing, and robust safety features.  

### 2.2 Drivers  
If I’m a driver, I need an easy-to-use app interface for managing ride requests and navigating to pickup and drop-off locations. I also need clear payment details and a way to track my earnings.  

---

## 3. Functional Requirements  

### 3.1 User Registration and Login  
As a rider or driver:  
- I must be able to register using my email address or phone number.  
- I must be able to log in with my credentials.  
- If I forget my password, I should have the option to reset it.  

### 3.2 User Profiles  

#### Riders:  
- I should be able to create and edit my profile, including contact information and payment methods.  
- I want access to my ride history and payment records.  

#### Drivers:  
- I should be able to set up my profile with details like my vehicle and availability.  
- I need access to my ride history, earnings, and ratings.  

### 3.3 Ride Booking and Management  

#### Riders:  
- I want to input my pickup and drop-off locations.  
- I should see available drivers nearby and their estimated arrival time (ETA).  
- I need a fare estimate before confirming a ride.  
- I want the option to cancel a ride before it starts.  
- I expect notifications for the driver’s arrival, ride start, and completion.  

#### Drivers:  
- I need ride requests with clear pickup and rider details.  
- I should be able to accept or decline requests.  
- I need in-app navigation for pickup and drop-off locations.  
- I should receive notifications about cancellations or changes.  

### 3.4 Payment Processing  

#### Riders:  
- I want to choose from multiple payment options (credit/debit cards, in-app wallet).  
- I need a payment confirmation after my ride.  
- I want access to my payment history.  

#### Drivers:  
- I want to track my earnings from rides.  
- I need payments sent directly to my chosen payout method.  

### 3.5 Ratings and Reviews  

#### Riders:  
- After a ride, I want to rate and review the driver.  

#### Drivers:  
- I should be able to rate and review riders after rides.  

### 3.6 Communication  
- I should be able to chat or call drivers/riders through the app.  
- I need notifications for messages received.  

### 3.7 Real-Time Tracking  

#### Riders:  
- I want to track the driver’s location in real-time.  

#### Drivers:  
- I should see the rider’s location for pickup.  

### 3.8 Customer Support  
- I need an easy way to contact support within the app.  
- FAQs and a help section should be available.  

### 3.9 Admin Panel  
If I were an admin:  
- I should be able to manage user accounts (approve, suspend, or delete them).  
- I want to view real-time data on active rides.  
- I need access to ride and payment histories for all users.  

---

## 4. Non-Functional Requirements  

### 4.1 Performance  
- I expect the app to load within 2 seconds under normal network conditions.  
- Ride requests, acceptances, and updates should process and display in under 1 second.  

### 4.2 Security  
#### Data Encryption  
- My data must be encrypted using AES-256 (at rest) and TLS 1.3 (in transit).  

#### Regulatory Compliance  
- The app must comply with Indian data protection laws like the **Personal Data Protection Bill (PDPB)** and the **IT Act, 2000**, ensuring explicit consent, rights for data access/modification/deletion, and data anonymization.  

#### User Authentication  
- Password policies must enforce strong passwords and support multi-factor authentication (e.g., OTPs).  

#### Access Control  
- Role-based access should ensure I only see features relevant to my role.  

### 4.3 Usability  
- The app must be intuitive, guiding me through ride booking and payments in three taps or less.  
- The UI should work consistently across devices, from 4-inch phones to 10-inch tablets.  
- Accessibility features like high contrast and touch-friendly buttons must comply with WCAG 2.1 Level AA.  

### 4.4 Reliability  
- The app should be available 99.9% of the time.  
- Backup systems must ensure no data loss during server failures.  

### 4.5 Scalability  
- The app must support up to 10,000 users initially and scale to 100,000 users in 12 months without performance issues.  
- A modular backend should allow new features without major disruptions.  

---

## 5. Assumptions and Dependencies  
- I assume users like me will have access to smartphones and stable internet.  
- Third-party services will handle maps, payments, and notifications.  

---

## 6. Acceptance Criteria  
- The app must pass all functional and non-functional tests.  
- Feedback during beta testing must be resolved before release.  
- The app must meet outlined security and performance standards.  

---

## 7. Conclusion  
This document defines my requirements for the Uber application. It will guide the team to create an app that meets my expectations as a user, whether I’m booking or offering rides, and aligns with the project’s goals.  

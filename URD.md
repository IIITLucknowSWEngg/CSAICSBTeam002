## User Requirements Document (URD)

### 1. Introduction

#### 1.1 Purpose
This document outlines my requirements for the Uber application. It will guide the design, development, and testing of the application to ensure that it meets my needs as a user, whether I’m booking rides as a rider or providing rides as a driver.

#### 1.2 Scope
Uber will be a ride-hailing mobile application connecting me with other users. As a rider, I’ll use it to book rides, track drivers in real-time, and pay seamlessly. As a driver, I’ll use it to manage ride requests and earn income efficiently.

#### 1.3 Definitions, Acronyms, and Abbreviations
- **Rider/User**: Someone like me who uses the app to book rides.
- **Driver**: Someone offering rides through the app.
- **Admin**: The person managing and overseeing the app’s operations.
- **ETA**: Estimated Time of Arrival.

#### 1.4 References
- Stakeholders.md
- Project.md

---

### 2. Rider-Specific Requirements

#### 2.1 Characteristics
As a rider, I’m familiar with basic app navigation on my smartphone. I expect a smooth, quick ride-booking experience with features like real-time updates, transparent pricing, and robust safety features.

#### 2.2 Functional Requirements

##### 2.2.1 User Registration and Login
- I must be able to register using my email address or phone number.
- I must be able to log in with my credentials.
- If I forget my password, I should have the option to reset it.

##### 2.2.2 User Profile
- I should be able to create and edit my profile, including contact information and payment methods.
- I want access to my ride history and payment records.

##### 2.2.3 Ride Booking and Management
- I want to input my pickup and drop-off locations.
- I should see available drivers nearby and their estimated arrival time (ETA).
- I need a fare estimate before confirming a ride.
- I want the option to cancel a ride before it starts.
- I expect notifications for the driver’s arrival, ride start, and completion.

##### 2.2.4 Payment Processing
- I want to choose from multiple payment options (credit/debit cards, in-app wallet).
- I need a payment confirmation after my ride.
- I want access to my payment history.

##### 2.2.5 Ratings and Reviews
- After a ride, I want to rate and review the driver.

##### 2.2.6 Communication
- I should be able to chat or call drivers through the app.
- I need notifications for messages received.

##### 2.2.7 Real-Time Tracking
- I want to track the driver’s location in real-time.

##### 2.2.8 Customer Support
- I need an easy way to contact support within the app.
- FAQs and a help section should be available.

---

### 3. Driver-Specific Requirements

#### 3.1 Characteristics
If I’m a driver, I need an easy-to-use app interface for managing ride requests and navigating to pickup and drop-off locations. I also need clear payment details and a way to track my earnings.

#### 3.2 Functional Requirements

##### 3.2.1 User Registration and Login
- I must be able to register using my email address or phone number.
- I must be able to log in with my credentials.
- If I forget my password, I should have the option to reset it.

##### 3.2.2 User Profile
- I should be able to set up my profile with details like my vehicle and availability.
- I need access to my ride history, earnings, and ratings.

##### 3.2.3 Ride Management
- I need ride requests with clear pickup and rider details.
- I should be able to accept or decline requests.
- I need in-app navigation for pickup and drop-off locations.
- I should receive notifications about cancellations or changes.

##### 3.2.4 Payment Processing
- I want to track my earnings from rides.
- I need payments sent directly to my chosen payout method.

##### 3.2.5 Ratings and Reviews
- I should be able to rate and review riders after rides.

##### 3.2.6 Communication
- I should be able to chat or call riders through the app.
- I need notifications for messages received.

##### 3.2.7 Real-Time Tracking
- I should see the rider’s location for pickup.

##### 3.2.8 Customer Support
- I need an easy way to contact support within the app.
- FAQs and a help section should be available.

---

### 4. Admin Requirements

#### 4.1 Characteristics
If I were an admin, I would oversee app operations, ensuring smooth interactions between riders and drivers.

#### 4.2 Functional Requirements
- I should be able to manage user accounts (approve, suspend, or delete them).
- I want to view real-time data on active rides.
- I need access to ride and payment histories for all users.

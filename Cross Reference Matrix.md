
# Cross-Reference Matrix

## Stakeholder Mapping to SRS and URD Sections

| Stakeholder          | SRS Section                            | URD Section                             |
|----------------------|----------------------------------------|-----------------------------------------|
| **Riders**            | 2.3 User Classes and Characteristics   | 4.1.1 User Registration & Profile       |
|                      | 3.2 Ride Booking                       | 4.1.2 Ride Booking & Ride Status       |
|                      | 3.4 Rating and Reviews                 | 4.1.5 Ride Completion                  |
|                      | 5.5 Usability                          | 4.1.4 Ride Booking & Payment Processing|
| **Drivers**           | 2.3 User Classes and Characteristics   | 4.2 Driver Registration & Profile      |
|                      | 3.3 Driver Acceptance                  | 4.2.3 Driver Ride Status               |
|                      | 3.4 Rating and Reviews                 | 4.2.4 Driver Earnings Dashboard        |
|                      | 5.2 Security Requirements              | 4.2.2 Driver Login & KYC               |
| **Admins**            | 2.3 User Classes and Characteristics   | 4.3 Admin Dashboard & Analytics        |
|                      | 4.4 Communication Interfaces           | 4.3 Admin Monitoring & Reporting       |
|                      | 4.5 Non-Functional Requirements        | 4.3 Admin User Management              |
|                      | 5.1 Performance Requirements           | 4.3 System Health & Scalability        |
| **Payment Gateway**   | 4.3 Software Interfaces                | 5.3 Payment Processing                 |
|                      | 5.3 Availability & Reliability         | 4.4 Payment Service Integration        |
| **Maps API**          | 4.3 Software Interfaces                | 4.1.2 Ride Navigation & Geolocation    |
| **SMS Gateway**       | 4.3 Software Interfaces                | 4.1.3 Ride Status Notification         |
| **Cloud Hosting**     | 5.3 Availability & Reliability         | 4.4 Infrastructure Design             |
|                      | 5.4 Scalability                        | 4.4 Backend Scalability               |

## Functional Requirement Mapping to SRS and URD

| Feature                          | SRS Section                                  | URD Section                                   |
|-----------------------------------|----------------------------------------------|-----------------------------------------------|
| **User Registration**             | 3.1 User Registration and Authentication     | 4.1.1 User Registration & Profile            |
| **User Login**                    | 3.1 User Registration and Authentication     | 4.1.2 Login & Profile Access                 |
| **Ride Booking**                  | 3.2 Ride Booking                            | 4.1.2 Ride Booking & Ride Status            |
| **Ride Status Update**            | 3.2 Ride Booking                            | 4.1.4 Ride Tracking                          |
| **Payment Processing**            | 3.3 Payment Processing                       | 4.1.5 Payment & Ride Completion              |
| **Rating and Reviews**            | 3.4 Rating and Reviews                       | 4.1.4 Ride Completion & Feedback             |
| **Driver Acceptance of Ride**     | 3.2 Ride Management                          | 4.2.3 Driver Ride Status                    |
| **Ride Completion**               | 3.2 Ride Management                          | 4.1.5 Ride Completion & User Billing         |
| **Admin Management**              | 4.1 Admin User Management                    | 4.3 Admin Dashboard                          |
| **System Scalability**            | 5.4 Scalability                              | 4.4 System Performance & Scalability         |

## Non-Functional Requirements Mapping

| Non-Functional Requirement         | SRS Section                                  | URD Section                                      |
|------------------------------------|----------------------------------------------|-------------------------------------------------|
| **Performance**                    | 5.1 Performance Requirements                 | 4.4 Performance Optimization                   |
| **Security**                       | 5.2 Security Requirements                    | 4.4 Data Security                               |
| **Availability & Reliability**     | 5.3 Availability and Reliability             | 4.4 System Availability                        |
| **Scalability**                    | 5.4 Scalability                              | 4.4 Scalability & Load Balancing               |
| **Usability**                      | 5.5 Usability                                | 4.1 User Experience (UI/UX)                    |
| **Maintainability**                | 5.6 Maintainability                          | 4.4 System Maintenance & Upgrades              |

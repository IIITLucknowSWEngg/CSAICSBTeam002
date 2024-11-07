![Component_Diagram_Driver](https://github.com/user-attachments/assets/6bbc5ab7-485c-491f-8612-ed2881d470ad)# System Context  Diagram Code

<img width="1418" alt="System Context" src="https://github.com/user-attachments/assets/10b7e891-2b59-4316-8ab9-85c8c00277dd">

```plantuml
@startuml

' External Actors
actor "Rider (User)" as Rider
actor "Driver (User)" as Driver
actor "Admin" as Admin
actor "Payment Gateway" as PaymentGateway
actor "Map Service" as MapService
actor "Notification Service" as NotificationService
actor "Customer Support" as CustomerSupport

' System Boundary: Uber Clone App
package "Uber Clone App" {

    ' Subsystems
    rectangle "User Registration \nand Authentication" as Registration
    rectangle "Ride Booking \nand Management" as RideBooking
    rectangle "Driver Functionality" as DriverFunctionality
    rectangle "Payment Integration" as Payment
    rectangle "Ratings and Reviews" as Ratings
    rectangle "Admin Panel" as AdminPanel
    rectangle "Push Notifications" as PushNotifications
    rectangle "In-App Chat \nand Support" as ChatSupport
    rectangle "Real-Time Location Tracking" as Tracking
    rectangle "Customer Support" as Support
}

' Relationships between actors and system components
Rider --> Registration : Sign Up/Login
Rider --> RideBooking : Request Ride
Rider --> Payment : Process Payment
Rider --> Ratings : Rate Driver
Rider --> PushNotifications : Receive Notifications
Rider --> ChatSupport : In-App Chat with Driver

Driver --> Registration : Register/Login
Driver --> RideBooking : Accept Ride Request
Driver --> DriverFunctionality : Manage Availability
Driver --> Payment : Receive Payment
Driver --> Ratings : Rate Rider
Driver --> PushNotifications : Receive Ride Notifications
Driver --> ChatSupport : In-App Chat with Rider

Admin --> AdminPanel : Manage Users/Drivers/Rides
Admin --> RideBooking : Monitor Rides
Admin --> Payment : Monitor Payments
Admin --> PushNotifications : Send Notifications
Admin --> Ratings : Manage Reviews

' External Interactions
Payment --> PaymentGateway : Process Payment Transactions
Tracking --> MapService : Use Maps for Navigation
PushNotifications --> NotificationService : Send Notifications
Support --> CustomerSupport : Handle User Issues

@enduml
```

# Container Diagram
## Driver
## Rider
## Admin

# Component Diagram
## Driver
![Component_Diagram_Driver](https://github.com/user-attachments/assets/44590bea-5bc8-4a37-9a49-e42059cab6db)
```plantuml
@startuml
' External Actors
actor "Driver (User)" as Driver
actor "Map Service" as MapService
actor "Notification Service" as NotificationService
actor "Payment Gateway" as PaymentGateway
actor "Rider (User)" as Rider
actor "Customer Support" as CustomerSupport

' System Boundary: Uber Clone App
package "Uber Clone App" {

    ' Subsystems specifically related to Driver
    rectangle "Driver Registration \nand Authentication" as DriverRegistration
    rectangle "Driver Profile Management" as DriverProfile
    rectangle "Ride Acceptance \nand Management" as RideManagement
    rectangle "Payment Processing" as DriverPayment
    rectangle "Driver Ratings \nand Feedback" as DriverRatings
    rectangle "Real-Time Location Tracking" as DriverTracking
    rectangle "Driver Notifications" as DriverNotifications
    rectangle "In-App Chat \nand Support" as DriverChatSupport
}

' Relationships between Driver and system components
Driver --> DriverRegistration : Register/Login
Driver --> DriverProfile : Manage Profile
Driver --> RideManagement : Accept/Decline Ride Requests
Driver --> DriverPayment : Track Earnings/Receive Payment
Driver --> DriverRatings : Rate Rider
Driver --> DriverNotifications : Receive Ride Notifications
Driver --> DriverChatSupport : Chat with Rider/Customer Support
Driver --> DriverTracking : Real-Time Location Sharing

' External Interactions
DriverTracking --> MapService : Access Navigation Maps
DriverPayment --> PaymentGateway : Process Driver Payments
DriverNotifications --> NotificationService : Send Notifications to Driver
DriverChatSupport --> CustomerSupport : Escalate Issues with Support
@enduml
```

## Rider
![Component_Diagram_Rider](https://github.com/user-attachments/assets/fea9fdc5-8e9b-4e06-8bb3-35069bd0ebea)

```plantuml
@startuml

' External Actors
actor "Rider (User)" as Rider
actor "Driver (User)" as Driver
actor "Admin" as Admin
actor "Payment Gateway" as PaymentGateway
actor "Map Service" as MapService
actor "Notification Service" as NotificationService
actor "Customer Support" as CustomerSupport

' System Boundary: Uber Clone App
package "Uber Clone App" {

    ' Subsystems
    rectangle "User Registration \nand Authentication" as Registration
    rectangle "Ride Booking \nand Management" as RideBooking
    rectangle "Payment Processing" as Payment
    rectangle "Driver Rating \nand Review" as Ratings
    rectangle "Push Notifications" as PushNotifications
    rectangle "In-App Chat \nand Support" as ChatSupport
    rectangle "Real-Time Location Tracking" as Tracking
    rectangle "Customer Support" as Support
}

' Relationships between actors and system components
Rider --> Registration : Sign Up/Login
Rider --> RideBooking : Request Ride
Rider --> Payment : Process Payment
Rider --> Ratings : Rate Driver
Rider --> PushNotifications : Receive Notifications
Rider --> ChatSupport : In-App Chat with Driver

Driver --> Registration : Register/Login
Driver --> RideBooking : Accept Ride Request
Driver --> Payment : Receive Payment
Driver --> Ratings : Rate Rider
Driver --> PushNotifications : Receive Ride Notifications
Driver --> ChatSupport : In-App Chat with Rider

Admin --> RideBooking : Monitor Rides
Admin --> Payment : Monitor Payments
Admin --> Ratings : Manage Reviews

' External Interactions
Payment --> PaymentGateway : Process Payment Transactions
Tracking --> MapService : Use Maps for Navigation
PushNotifications --> NotificationService : Send Notifications
Support --> CustomerSupport : Handle User Issues

@enduml
```


## Admin

<img width="1414" alt="Component DIagram - Admin" src="https://github.com/user-attachments/assets/fc1ce63e-cf5c-42a4-8c1f-d058d3df9678">

```plantuml
@startuml

' Define the system components for the Admin Panel
package "Admin Panel" {
    component "Dashboard" as Dashboard
    component "User Management" as UserManagement
    component "Driver Management" as DriverManagement
    component "Ride Monitoring" as RideMonitoring
    component "Payment Management" as PaymentManagement
    component "Reports and Analytics" as ReportsAnalytics
    component "Notification Management" as NotificationManagement
}

' External services used by the Admin Panel
database "User Database" as UserDB
database "Driver Database" as DriverDB
database "Ride Database" as RideDB
database "Payment Database" as PaymentDB
component "Notification Service" as NotificationService
component "Payment Gateway" as PaymentGateway

' Relationships between Admin Panel components
Dashboard --> UserManagement : Access User Data
Dashboard --> DriverManagement : Manage Drivers
Dashboard --> RideMonitoring : Monitor Active Rides
Dashboard --> PaymentManagement : View Payment Info
Dashboard --> ReportsAnalytics : Generate Reports
Dashboard --> NotificationManagement : Send Notifications

' Internal component interactions
UserManagement --> UserDB : Read/Write User Data
DriverManagement --> DriverDB : Read/Write Driver Data
RideMonitoring --> RideDB : Access Ride Data
PaymentManagement --> PaymentDB : Access Payment Data
ReportsAnalytics --> UserDB : Generate User Reports
ReportsAnalytics --> DriverDB : Generate Driver Reports
ReportsAnalytics --> RideDB : Generate Ride Reports
ReportsAnalytics --> PaymentDB : Generate Payment Reports

' External interactions
PaymentManagement --> PaymentGateway : Process Payment Refunds
NotificationManagement --> NotificationService : Send Notifications to Users

@enduml

```

# Deployment Diagram Code

![Deployment Diagram](Deployment.png)

```plantuml
@startuml
title Deployment Diagram - Uber Clone System

node "Rider's Mobile Device" {
    [Rider Mobile App] <<Mobile App>>
}

node "Driver's Mobile Device" {
    [Driver Mobile App] <<Mobile App>>
}

node "Admin's PC" {
    [Admin Web Dashboard] <<Web App>>
}

node "Web Server" {
    [Ride Management Service] <<Microservice>>
    [Payment Service] <<Microservice>>
    [User Management Service] <<Microservice>>
    [Real-Time Tracking Service] <<Microservice>>
}

node "Database Server" {
    database "User Database" as UserDB
    database "Ride Database" as RideDB
    database "Payment Database" as PaymentDB
}

cloud "Third-Party Services" {
    [Payment Gateway] <<External Service>>
    [Map/GPS Service] <<External Service>>
}

' Connections
[Rider Mobile App] --> [Ride Management Service] : "Request rides"
[Rider Mobile App] --> [Payment Service] : "Process payment"
[Rider Mobile App] --> [Real-Time Tracking Service] : "Track driver"
[Rider Mobile App] --> [User Management Service] : "Manage profile"

[Driver Mobile App] --> [Ride Management Service] : "Accept/Decline ride"
[Driver Mobile App] --> [Real-Time Tracking Service] : "Navigate to rider"
[Driver Mobile App] --> [User Management Service] : "Manage profile"
[Driver Mobile App] --> [Payment Service] : "View earnings"

[Admin Web Dashboard] --> [Ride Management Service] : "Monitor rides"
[Admin Web Dashboard] --> [User Management Service] : "Manage users"
[Admin Web Dashboard] --> [Payment Service] : "Monitor payments"

[Ride Management Service] --> UserDB : "Read/Write user and ride data"
[Payment Service] --> PaymentDB : "Read/Write payment data"
[User Management Service] --> UserDB : "Manage user profiles"
[Real-Time Tracking Service] --> RideDB : "Read/Write location data"

[Payment Service] --> [Payment Gateway] : "Process payment"
[Real-Time Tracking Service] --> [Map/GPS Service] : "Access map and GPS data"

@enduml
```





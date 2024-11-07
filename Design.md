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


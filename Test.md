### **Feature: User Registration**

| **Test ID**    | **TC-REG-001**                                               |
|----------------|--------------------------------------------------------------|
| **Description**| Verify that a user can successfully register with valid information. |
| **Precondition** | User is on the registration page.                           |
| **Steps**      | 1. The user enters valid information (name, email, password). <br> 2. The user submits the registration form. |
| **Expected Result** | The user should be successfully registered. <br> The user should be redirected to the login/home/profile/redirectedTo page. |
| **Status**     | Pending/Pass/Fail                                            |



## Chai.js Code:

```javascript
const chai = require('chai');
const expect = chai.expect;
const registrationPage = require('../pages/registrationPage');

describe('User Registration', function() {
  it('should register user successfully', function() {
    registrationPage.open();
    registrationPage.fillRegistrationForm('John Doe', 'john@example.com', 'password123');
    registrationPage.submitForm();
    expect(registrationPage.getSuccessMessage()).to.equal('Registration successful');
    expect(browser.getUrl()).to.include('/login');
  });
});
```
---

### **Feature: User Login**

| **Test ID**    | **TC-LOG-001**                                               |
|----------------|--------------------------------------------------------------|
| **Description**| Verify that a user can successfully log in with valid credentials. |
| **Precondition** | User is on the login page.                                  |
| **Steps**      | 1. The user enters valid credentials (email, password). <br> 2. The user submits the login form. |
| **Expected Result** | The user should be successfully logged in. <br> The user should be redirected to the dashboard. |
| **Status**     | Pending/Pass/Fail                                            |


## Chai.js Code:

```javascript
const chai = require('chai');
const expect = chai.expect;
const loginPage = require('../pages/loginPage');

describe('User Login', function() {
  it('should login user successfully', function() {
    loginPage.open();
    loginPage.enterCredentials('john@example.com', 'password123');
    loginPage.submitLogin();
    expect(loginPage.getWelcomeMessage()).to.include('Welcome, John Doe');
    expect(browser.getUrl()).to.include('/dashboard');
  });
});
```
---
### **Feature: Ride Booking**

| **Test ID**    | **TC-RB-001**                                               |
|----------------|--------------------------------------------------------------|
| **Description**| Verify that the user can successfully book a ride.           |
| **Precondition** | User is logged in and on the ride booking page.             |
| **Steps**      | 1. The user enters valid pickup and drop-off locations. <br> 2. The user selects a payment method. <br> 3. The user submits the booking. |
| **Expected Result** | The ride should be successfully booked. <br> The user should receive a confirmation message. |
| **Status**     | Pending/Pass/Fail                                            |



## Chai.js Code:

```javascript
const chai = require('chai');
const expect = chai.expect;
const ridePage = require('../pages/ridePage');

describe('Ride Booking', function() {
  it('should book a ride successfully', function() {
    ridePage.open();
    ridePage.enterLocations('123 Main St', '456 Elm St');
    ridePage.selectPaymentMethod('Credit Card');
    ridePage.submitBooking();
    expect(ridePage.getConfirmationMessage()).to.equal('Ride booked successfully');
    expect(browser.getUrl()).to.include('/ride-details');
  });
});
```
---

### *Feature: Driver Acceptance of Ride*

| *Test ID*    | *TC-DR-001*                                               |
|----------------|-------------------------------------------------------------|
| *Description*| Verify that the driver accepts a ride request successfully. |
| *Precondition* | Driver is logged in. <br> There is a ride request available. |
| *Steps*      | 1. The driver accepts the ride request. |
| *Expected Result* | The ride status should be updated to "Accepted". <br> The user should receive a notification. |
| *Status*     | Pending/Pass/Fail                                            |
## Chai.js Code:

```javascript
const chai = require('chai');
const expect = chai.expect;
const driverPage = require('../pages/driverPage');
const userNotification = require('../pages/userNotification');

describe('Driver Acceptance of Ride', function() {
  it('should update ride status and notify user', function() {
    driverPage.open();
    driverPage.acceptRide();
    expect(driverPage.getRideStatus()).to.equal('Accepted');
    expect(userNotification.getNotification()).to.equal('Your ride has been accepted');
  });
});

```
---


### **Feature: Payment Processing**

| **Test ID**    | **TC-PP-001**                                               |
|----------------|--------------------------------------------------------------|
| **Description**| Verify that the user can successfully complete payment for a ride. |
| **Precondition** | User has a ride booked.                                     |
| **Steps**      | 1. The user selects a payment method and enters payment details. <br> 2. The user submits the payment. |
| **Expected Result** | The payment should be processed successfully. <br> The user should receive a payment confirmation. |
| **Status**     | Pending/Pass/Fail                                            |


## Chai.js Code:

```javascript
const chai = require('chai');
const expect = chai.expect;
const paymentPage = require('../pages/paymentPage');

describe('Payment Processing', function() {
  it('should process payment successfully', function() {
    paymentPage.open();
    paymentPage.enterPaymentDetails('1234 5678 9012 3456', '12/25', '123');
    paymentPage.submitPayment();
    expect(paymentPage.getPaymentConfirmation()).to.equal('Payment successful');
    expect(browser.getUrl()).to.include('/payment-confirmation') ;
  });
});
```
---


### **Feature: Ride Status Update**

| **Test ID**    | **TC-RSU-001**                                              |
|----------------|-------------------------------------------------------------|
| **Description**| Verify that the user can view the current status of their ride. |
| **Precondition** | User has a ride booked.                                    |
| **Steps**      | 1. The user navigates to the ride status page. <br> 2. The user checks the current status of the ride. |
| **Expected Result** | The user should see the current status of their ride (e.g., "Ride is on the way"). |
| **Status**     | Pending/Pass/Fail                                            |



## Chai.js Code:

```javascript
const chai = require('chai');
const expect = chai.expect;
const rideStatusPage = require('../pages/rideStatusPage');

describe('Ride Status Update', function() {
  it('should show the correct ride status', function() {
    rideStatusPage.open();
    rideStatusPage.checkStatus();
    expect(rideStatusPage.getStatus()).to.equal('Ride is on the way');
  });
});
```
---

### **Feature: User Profile Management**

| **Test ID**    | **TC-UPM-001**                                               |
|----------------|--------------------------------------------------------------|
| **Description**| Verify that the user can successfully update their profile. |
| **Precondition** | User is logged in.                                          |
| **Steps**      | 1. The user navigates to the profile page. <br> 2. The user updates their profile information (name, email). <br> 3. The user saves the changes. |
| **Expected Result** | The profile should be updated successfully. |
| **Status**     | Pending/Pass/Fail                                            |


## Chai.js Code:

```javascript
const chai = require('chai');
const expect = chai.expect;
const profilePage = require('../pages/profilePage');

describe('User Profile Management', function() {
  it('should update user profile successfully', function() {
    profilePage.open();
    profilePage.updateProfile('John Updated', 'johnupdated@example.com');
    expect(profilePage.getSuccessMessage()).to.equal('Profile updated successfully');
  });
});
```
---

### **Feature: Ride Completion**

| **Test ID**    | **TC-RC-001**                                               |
|----------------|-------------------------------------------------------------|
| **Description**| Verify that the driver completes the ride and the user is billed. |
| **Precondition** | The driver has completed the ride.                         |
| **Steps**      | 1. The driver ends the ride.                                |
| **Expected Result** | The user should be billed for the ride. <br> The user should receive a payment receipt. |
| **Status**     | Pending/Pass/Fail                                            |
## Chai.js Code:

```javascript
const chai = require('chai');
const expect = chai.expect;
const driverPage = require('../pages/driverPage');
const paymentPage = require('../pages/paymentPage');

describe('Ride Completion', function() {
  it('should complete the ride and bill the user', function() {
    driverPage.open();
    driverPage.completeRide();
    expect(driverPage.getRideStatus()).to.equal('Completed');
    expect(paymentPage.getReceipt()).to.include('Payment successfully processed');
  });
});
```
---

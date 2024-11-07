# Feature: User Registration

## Scenario: User registers successfully

### Given:
The user is on the registration page.

### When:
The user enters valid information (name, email, password).

### Then:
The user should be successfully registered.  
The user should be redirected to the login page.

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

# Feature: User Login

## Scenario: User logs in with valid credentials

### Given:


The user is on the login page.

### When:
The user enters valid credentials (email, password).

### Then:
The user should be successfully logged in.  
The user should be redirected to the dashboard.

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


# Feature: Ride Status Update

## Scenario: User checks the status of their ride

### Given:
The user has a ride booked.

### When:
The user navigates to the ride status page.

### Then:
The user should see the current status of their ride.

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
# Feature: User Profile Management

## Scenario: User updates their profile successfully

### Given:
The user is logged in.

### When:
The user navigates to the profile page.  
The user updates their profile information.

### Then:
The profile should be updated successfully.

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

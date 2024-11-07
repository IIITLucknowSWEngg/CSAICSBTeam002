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


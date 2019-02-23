# TOTP.js
A Javascript class for generating TOTP passwords (time-based one-time passwords) automatically (think Google Authenticator).
OTP is calculated based on a provided 16-character key (secret).
This is the open-source algorithm that Google Authenticator and other 2FA-enabled apps utilize.
This script is based on a code snippet published by user "russ" on http://blog.tinisles.com.

## Written by:
Jay Simons
https://Cloudulus.Media

This class requires sha.js, which can be found here: http://caligatio.github.io/jsSHA/sha.js
 
# Usage Example:

Instantiates object and keeps it alive in DOM
```javascript
var totp = new TOTP('user secret', 'optional user name for display');
```

## Getters:

```javascript
// Returns current OTP
totp.getOTP();

// Returns URL to Google Charts QR Code (for scanning into Google Authenticator)
totp.getQR();

// Returns time (in seconds) until next OTP update
totp.getCountDown();
```

## Setters:

```javascript
// Sets 16-digit user secret (key)
totp.setKey(secretKey);

// Sets logging output to console.log()
totp.setLog(true|false);

// Sets username display (for QR code), default is "user@example.com" if not set
totp.getUser(username);
```

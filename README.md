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
 
`var totp = new TOTP('user secret', 'optional user name for display'); // Instantiates object and keeps it alive in DOM`

## Getters:

`totp.getOTP() // Returns current OTP`
`totp.getQR() // Returns URL to Google Charts QR Code (for scanning into Google Authenticator)`
`totp.getCountDown() // Returns time (in seconds) until next OTP update`

## Setters:

`totp.setKey(secretKey) // Sets 16-digit user secret (key)`
`totp.setLog(true|false) // Sets logging output to console.log()`
`totp.getUser(username) // Sets username display (for QR code), default is "user@example.com" if not set`
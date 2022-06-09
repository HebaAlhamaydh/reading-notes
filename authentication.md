# Authentication
Authentication  is the process of recognizing a user’s identity (verifies who the user is).The authentication process always runs at the start of the application, before the permission, and before any other code is allowed to proceed.
# Securing Passwords with Bcrypt Hashing Function
**Cryptographic hash algorithms** MD5, SHA1, SHA256, SHA512, SHA-3 are general purpose hash functions, designed to calculate a digest of huge amounts of data in as short a time as possible.

**Hashing** is the process of transforming any given key or a string of characters into another value.
  Hashing is the greatest way for protecting passwords and to be more safe for ensuring the safety of data or password.
  The useful of hashing is that if  the database is stealed  with hashed passwords, they only make off with the hashes and not the real plaintext passwords
  # PROBLEMS WITH CRYPTOGRAPHIC HASH ALGORITHM
  - **Brute Force attack:** is a hacking method that uses test and error to crack passwords, login certification, and encryption keys.
  - **Hash Collision attack** :attempt to find two input strings of a hash function that produce the same hash result
  # BCrypt, IT's SLOW AND STRONG AS HELL
  PBKDF2 and BCrypt, both of these algorithms use a technique called Key Stretching.
  Bcrypt is an adaptive hash function based on the Blowfish symmetric block cipher cryptographic algorithm and introduces a work factor
  # Basic access authentication
  a method for an HTTP user agent to provide a user name and password when making a request.  A request contains a header field in the form of Authorization: Basic <credentials>, where credentials is the Base64 encoding of ID and password joined by a single colon :
  # Features
  HTTP Basic authentication (BA) implementation is the simplest technique for enforcing access controls to web resources because it does not require cookies, session identifiers, or login pages; rather, HTTP Basic authentication uses standard fields in the HTTP header.
  # Security
  Because the BA field has to be sent in the header of each HTTP request, the web browser needs to cache credentials for a reasonable period of time to avoid constantly prompting the user for their username and password
  # Protocol
  - Server side

The WWW-Authenticate header field for basic authentication is constructed as following:
```
WWW-Authenticate: Basic realm="User Visible Realm", charset="UTF-8"
```
 - Client side
 ```
 Authorization: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ==
 ```
 # Authentication General Guidelines
 ## User IDs
 Make sure your usernames/user IDs are case-insensitive, unique


# Authentication Solution and Sensitive Accounts
- Do NOT allow login with sensitive accounts to any front-end user-interface.
- Do NOT use the same authentication solution used internally for unsecured access .
# Authentication and Error Messages
Using any of the authentication mechanisms (login, password reset or password recovery), an application must respond with a generic error message regardless of :
- The user ID or password was incorrect.
- The account does not exist.
- The account is locked or disabled.

The account registration feature should also be taken into sight, and the same approach of generic error message can be utilized concerning the case in which the user exists.

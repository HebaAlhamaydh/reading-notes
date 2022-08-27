## Login and Auth 
##  What is Role-Based Access Control (RBAC)?
Role-based access control (RBAC) restricts network access based on a person's role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network.
## EXAMPLES OF ROLE-BASED ACCESS CONTROL
- **Management role scope**– it limits what objects the role group is allowed to manage.
- **Management role group** – you can add and remove members.
- **Management role** – these are the types of tasks that can be performed by a specific role group.
- **Management role assignment** – this links a role to a role group.
## BENEFITS OF RBAC
- Reducing administrative work and IT support.
- Maximizing operational efficiency.
- Improving compliance.
## BEST PRACTICES FOR IMPLEMENTING RBAC
- Current Status.
- Current Roles.
- Write a Policy.
- Make Changes.
- Continually Adapt.
## react-cookie 
Getting started
```js
npm install react-cookie
```
```js
<script
  crossorigin
  src="https://unpkg.com/react@16/umd/react.production.js"
></script>
<script
  crossorigin
  src="https://unpkg.com/universal-cookie@3/umd/universalCookie.min.js"
></script>
<script
  crossorigin
  src="https://unpkg.com/react-cookie@3/umd/reactCookie.min.js"
></script>
```
## useCookies([dependencies])
```js
const [cookies, setCookie, removeCookie] = useCookies(['cookie-name']);
```
## Cookies Methods : 

### `get(name, [options])`

Get a cookie value

- name (string): cookie name
- options (object):
doNotParse (boolean): do not convert the cookie into an object no matter what


### `getAll([options])`

Get all cookies

- options (object):
    - doNotParse (boolean): do not convert the cookie into an object no matter what

### `set(name, value, [options])`

Set a cookie value

- name (string): cookie name
- value (string|object): save the value and stringify the object if needed
- options (object): Support all the cookie options from RFC 6265
    - path (string): cookie path, use / as the path if you want your cookie to be accessible on all pages
    - expires (Date): absolute expiration date for the cookie
    - maxAge (number): relative max age of the cookie from when the client receives it in seconds
    - domain (string): domain for the cookie (sub.domain.com or .allsubdomains.com)
    - secure (boolean): Is only accessible through HTTPS?
    - httpOnly (boolean): Can only the server access the cookie? Note: You cannot get or set httpOnly cookies from the browser, only the server.
    - sameSite (boolean|none|lax|strict): Strict or Lax enforcement

### `remove(name, [options])`

Remove a cookie

- name (string): cookie name
- options (object): Support all the cookie options from RFC 6265
    - path (string): cookie path, use / as the path if you want your cookie to be accessible on all pages
    - expires (Date): absolute expiration date for the cookie
    - maxAge (number): relative max age of the cookie from when the client receives it in seconds
    - domain (string): domain for the cookie (sub.domain.com or .allsubdomains.com)
    - secure (boolean): Is only accessible through HTTPS?
    - httpOnly (boolean): Can only the server access the cookie? Note: You cannot get or set httpOnly cookies from the browser, only the server.
    - sameSite (boolean|none|lax|strict): Strict or Lax enforcement

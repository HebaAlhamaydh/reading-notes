## Introducing Node
## What is Node?
Runtime environment run javascript code outside browser.Uses V8 engine.Allows developers to build server-side tools and applications in JavaScript.

## Introducing Express
Javascript framework for Nodejs.Make build server easier.provides methods to specify what function is called for a particular HTTP verb (GET, POST, SET, etc.) and URL("Route").

**Import the express module and create an Express application**
```
const express = require('express');
const app = express();
````
**Creating Routes**: The app.get() method specifies a callback function that will be invoked whenever there is an HTTP GET request with a path ('/') relative to the site root.
```
app.get('/', function(req, res) {
  res.send('Hello World!')
});
```
**Server always listening and ready to recive request**:
```
app.listen(port, function() {
  console.log(`Example app listening on port ${port}!`)
});
```
## About npm
Stand for **Node Package Manager** 

npm consists of:
- **website**: to discover packages, set up profiles. 
- **Command Line Interface (CLI**:runs from a terminal, and is how most developers interact with npm.
- **registry**: is a large public database of JavaScript softwar.
## What is TDD?
**“Test-driven development”**: coding, testing (in the form of writing unit tests) and design (in the form of refactoring).
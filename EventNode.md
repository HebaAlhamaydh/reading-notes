## Event-Driven Programming in Node.js

Event-Driven Programming is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision.

Event-driven programming is used to synchronize the occurrence of multiple events and to make the program as simple as possible.

## Event-Driven Programming makes use of the following concepts:
-A callback function ( called an event handler) is called when an event is triggered.
- A Main Loop listens for event triggers and calls the associated event handler for that event.

## EventEmitter
allows us to get started incorporating Event-Driven Programming in our project right away.
##  Create a New EventEmitter Object
```
const EventEmitter = require('events').EventEmitter;
const myEventEmitter = new EventEmitter;
```
## Chat room example:
alert everyone when a new user joins the chat room
``` 
const EventEmitter = require('events').EventEmitter;
const chatRoomEvents = new EventEmitter;

function userJoined(username){
  // Assuming we already have a function to alert all users.
  alertAllUsers('User ' + username + ' has joined the chat.');
}

// Run the userJoined function when a 'userJoined' event is triggered.
chatRoomEvents.on('userJoined', userJoined);
```
EventEmitter has an emit method that we we use to trigger the event. We would want to trigger this event from within a login function inside of our chatroom module.
```
function login(username){
  chatRoomEvents.emit('userJoined', username);
}
```
## Removing Listeners
To remove event listeners in EventEmitter we can use the removeListener or removeAllListeners method.
### we remove it for :
- Performance reasons.
- Avoid memory leaks.
## Example
```
const EventEmitter = require('events').EventEmitter;
const chatRoomEvents = new EventEmitter;

function displayMessage(message){
  document.write(message);
}

function userJoined(username){
  chatRoomEvents.on('message', displayMessage);
}

chatRoomEvents.on('userJoined', userJoined);
```
 to remove the displayMessage function from the message event’s list of handlers:
 ```
 chatRoomEvents.removeListener('message', displayMessage);
 ```
 ## Object Oriented Programming with Event-Driven Programming
 ```
 const EventEmitter = require('events').EventEmitter;
const myGatorEvents = new EventEmitter;

class Food {
  constructor(name) {
    this.name = name;
    // Become eaten when gator emits 'gatorEat'
    myGatorEvents.on('gatorEat', this.becomeEaten);
  }

  becomeEaten(){
    return 'I have been eaten.';
  }
}

var bacon = new Food('bacon');

const gator = {
  eat() {
    myGatorEvents.emit('gatorEat');
  }
}
```
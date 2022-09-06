

# Asynchronous Actions

## Async Logic and Data Fetching
a Redux store doesn't know anything about async logic. It only knows how to synchronously dispatch actions, update the state by calling the root reducer function, and notify the UI that something has changed. Any asynchronicity has to happen outside the store.

Redux reducers must never contain "side effects". 
+ side effect: is any change to state or behavior that can be seen outside of returning a value from a function. 

Example on side effects:
+ Logging a value to the console
+ Saving a file
+ Setting an async timer
+ Making an AJAX HTTP request
+ Modifying some state that exists outside of a function, or mutating arguments to a function.
+ Generating random numbers or unique random IDs (such as Math.random() or Date.now()).

## Redux middleware were designed to enable writing logic that has side effects.

Redux middleware can do anything when it sees a dispatched action: log something, modify the action, delay the action, make an async call, and more. Also, since middleware form a pipeline around the real store.dispatch function, this also means that we could actually pass something that isn't a plain action object to dispatch, as long as a middleware intercepts that value and doesn't let it reach the reducers.

Middleware also have access to dispatch and getState. That means you could write some async logic in a middleware, and still have the ability to interact with the Redux store by dispatching actions.

## Redux Thunk
Thunk middleware for Redux. It allows writing functions with logic inside that can interact with a Redux store's dispatch and getState methods.

### Manual Setup to add Redux Thunk

`npm install redux-thunk`

Then, to enable Redux Thunk, use `applyMiddleware()`:


```js
import { createStore, applyMiddleware } from 'redux'
import thunk from 'redux-thunk'
import rootReducer from './reducers/index'

const store = createStore(rootReducer, applyMiddleware(thunk))
```



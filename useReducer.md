## useReducer
## Name an alternative to the useState Hook
An alternative to useState. Accepts a reducer of type (state, action) => newState, and returns the current state paired with a dispatch method.
```js
const [state, dispatch] = useReducer(reducer, initialArg, init);
```
## Why might the useReducer Hook be preferable to the useState Hook?
✔️ useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one.

✔️ also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.
## What are two ways to set the initial state?
There are two different ways to initialize useReducer state.
- The simplest way is to pass the initial state as a second argument
```js
const [state, dispatch] = useReducer(
    reducer,
    {count: initialCount}
  );
  ```
  - you can pass an init function as the third argument. The initial state will be set to init(initialArg).
  ```js
  function init(initialCount) {
  return {count: initialCount};
}

function reducer(state, action) {
  switch (action.type) {
    case 'increment':
      return {count: state.count + 1};
    case 'decrement':
      return {count: state.count - 1};
    case 'reset':
      return init(action.payload);
    default:
      throw new Error();
  }
}

function Counter({initialCount}) {
  const [state, dispatch] = useReducer(reducer, initialCount, init);
  return (
    <>
      Count: {state.count}
      <button
        onClick={() => dispatch({type: 'reset', payload: initialCount})}>
        Reset
      </button>
      <button onClick={() => dispatch({type: 'decrement'})}>-</button>
      <button onClick={() => dispatch({type: 'increment'})}>+</button>
    </>
  );
}

```
## In terms of state, what does useReducer expect to receive as a parameter?
The useReducer Hook is used to store and update states, just like the useState Hook. It accepts a reducer function as its first parameter and the initial state as the second:
```js
const [count, dispatch] = useReducer(reducer, initialState);
```
The reducer function itself accepts two parameters and returns one value. The first parameter is the current state, and the second is the action. The state is the data we are manipulating. The reducer function receives an action, which is executed by a dispatch function:
```js
function reducer(state, action) { }

dispatch({ type: 'increment' })
```

## What does useReducer return?
useReducer returns an array that holds the current state value and a dispatch function to which you can pass an action and later invoke it
## Explain dispatch to a non-technical recruiter.
The dispatch function accepts an object that represents the type of action we want to execute when it is called. Basically, it sends the type of action to the reducer function to perform its job, which, of course, is updating the state

## useEffect Hook
## What purpose does useEffect serve in a function component compared to its counterpart(s) in class components?
The Effect Hook lets you perform side effects in function components:
```js
import React, { useState, useEffect } from 'react';

function Example() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    document.title = `You clicked ${count} times`;
  });

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```
we set the document title to a custom message
 ## Examples of side effects:

- Data fetching.
- Setting up a subscription.
- Manually changing the DOM in React components.
## Example Using Classes
In React class components, the render method itself shouldn’t cause side effects. It would be too early — we typically want to perform our effects after React has updated the DOM.
This is why in React classes, we put side effects into **componentDidMount** and **componentDidUpdate**.
```js
class Example extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0
    };
  }

  componentDidMount() {
    document.title = `You clicked ${this.state.count} times`;
  }
  componentDidUpdate() {
    document.title = `You clicked ${this.state.count} times`;
  }

  render() {
    return (
      <div>
        <p>You clicked {this.state.count} times</p>
        <button onClick={() => this.setState({ count: this.state.count + 1 })}>
          Click me
        </button>
      </div>
    );
  }
}
```
##  Example Using Hooks
```js
import React, { useState, useEffect } from 'react';

function Example() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    document.title = `You clicked ${count} times`;
  });

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```
## What does useEffect do?
By using this Hook, you tell React that your component needs to do something after render.
## Why is useEffect called inside a component?
Placing useEffect inside the component lets us access the count state variable (or any props) right from the effect.
## Does useEffect run after every render? 
Yes! By default, it runs both after the first render and after every update.

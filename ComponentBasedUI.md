## React
React is a JavaScript library for building user interfaces
## The smallest React example
```
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<h1>Hello, world!</h1>);
```
## What are the building blocks of a React app?
- Elements.
- Components.
## What is the difference between an element and a React component?
- **Elements** are the smallest building blocks of React apps.It contains both type and property. It may contain other Elements in its props. It does not have any methods, making it light and faster to render than components.
- **React component** It is independent and reusable. It returns the virtual DOM of the element. One may or may not pass any parameter while creating a component.
  - The simplest way to define a component
  ```
  function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

## What are some advantages of React’s component based architecture?
- Reusability
- Repetition
- Faster development
## Introducing JSX
## What is JSX and why do we use it?
JSX stands for JavaScript XML.

JSX allows us to write HTML in React.

JSX makes it easier to write and add HTML in React.

React doesn’t require using JSX, but most people find it helpful as a visual aid when working with UI inside the JavaScript code. It also allows React to show more useful error and warning messages.

## Embedding Expressions in JSX
```
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;
```
## Rendering Elements
The only way to update the UI is to create a new element, and pass it to root.render(). Consider this ticking clock example:
```
const root = ReactDOM.createRoot(
  document.getElementById('root')
);

function tick() {
  const element = (
    <div>
      <h1>Hello, world!</h1>
      <h2>It is {new Date().toLocaleTimeString()}.</h2>
    </div>
  );
  root.render(element);
}
setInterval(tick, 1000);
```
## If changes are made to the UI, what does React update?
React Only Updates What’s Necessary.

React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.

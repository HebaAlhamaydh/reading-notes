## Hook
Hooks are a new addition in React 16.8. They let you use state and other React features without writing a class.

## What was the motivation for introducing Hooks?
React Hooks are the improvement points that the React team has gradually realized in the development practice. The thinking behind it involves the comparison of class components and function components .
## What changes are important regarding implementing Hooks versus Component Classes?

## Hooks allow you to reuse stateful logic without changing
Hooks allow you to reuse stateful logic without changing your component hierarchy. This makes it easy to share Hooks among many components or with the community.
## Name two rules imposed by React Hook usage.
- Only call Hooks at the top level. Don’t call Hooks inside loops, conditions, or nested functions.
- Only call Hooks from React function components. Don’t call Hooks from regular JavaScript functions. 

## What is a Hook? 
A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components. We’ll learn other Hooks later.
## When would I use a Hook? 
If you write a function component and realize you need to add some state to it, previously you had to convert it to a class. Now you can use a Hook inside the existing function component. We’re going to do that right now

## If you were to add React state to a function component by declaring a state variable:
### What does calling useState do?
It declares a “state variable”.
useState is a new way to use the exact same capabilities that this.state provides in a class. Normally, variables “disappear” when the function exits but state variables are preserved by React.

### What do we pass to useState as an argument?
The only argument to the useState() Hook is the initial state.Unlike with classes, the state doesn’t have to be an object. We can keep a number or a string if that’s all we need.If we wanted to store two different values in state, we would call useState() twice
### What does useState return?
It returns a pair of values: the current state and a function that updates it. 


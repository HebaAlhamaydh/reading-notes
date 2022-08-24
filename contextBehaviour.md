## With regard to the React Context API, what does a “provider” do?
Every Context object comes with a Provider React component that allows consuming components to subscribe to context changes.

The Provider component accepts a value prop to be passed to consuming components that are descendants of this Provider. One Provider can be connected to many consumers. 
```js
<MyContext.Provider value={/* some value */}>
````
## With regard to the React Context API, how would we implement a “consumer” role?
A React component that subscribes to context changes. Using this component lets you subscribe to a context within a function component.

Requires a function as a child. The function receives the current context value and returns a React node. The value argument passed to the function will be equal to the value prop of the closest Provider for this context above in the tree. If there is no Provider for this context above, the value argument will be equal to the defaultValue that was passed to createContext().
```js
<MyContext.Consumer>
  {value => /* render something based on the context value */}
</MyContext.Consumer>
```
###  Specifically with Context, how are we “wrapping” components to achieve our goals?
It turns out that our custom hook from before is nothing more than a small wrapper around the useContext internal React hook, which consumes our new context. Our provider exposes the state mutator setAlerts directly, but we need something much higher level. We don’t want our components fumbling around with how to add an alert without destroying existing ones, and so on. Think of setAlerts as a private method, and we need to expose a public method that abstracts away the noise.



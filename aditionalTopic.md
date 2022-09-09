# Redux - Additional Topics

## Getting Started with Redux Toolkit

The Redux Toolkit package is intended to be the standard way to write Redux logic. It was originally created to help address three common concerns about Redux:

+ Configuring a Redux store is too complicated
+ I have to add a lot of packages to get Redux to do anything useful
+ Redux requires too much boilerplate code

## Installation​

`npx create-react-app my-app --template redux`

### To An Existing App

`npm install @reduxjs/toolkit`

## Hookstate
The simple but incredibly fast and flexible state management that is based on React state hook

### Installation and dependencies
`npm install --save @hookstate/core`

### Ten minute introduction to MobX and React

State is the heart of each application and there is no quicker way to create buggy, unmanageable applications than by producing an inconsistent state or state that is out-of-sync with local variables that linger around. Hence many state management solutions try to restrict the ways in which you can modify state, for example by making state immutable. But this introduces new problems; data needs to be normalized, referential integrity can no longer be guaranteed and it becomes next to impossible to use powerful concepts like classes in case you fancy those.

![getting-started-assets](https://mobx.js.org/assets/getting-started-assets/overview.png)
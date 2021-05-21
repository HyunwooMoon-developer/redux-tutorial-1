# REDUX

## Integrating Redux with a UI

- Create a Redux store
- Subscribe to updates
- Inside the subscription callback (Get the current store state, Extract the data needed by this piece of UI, Update the UI with the data)
- If necessary, render the UI with initial state
- Respond to UI inputs by dispatching Redux actions

## Reason to Use React Redux

1. It is the Official Redux UI Bindings for React

While Redux can be used with any UI layer, it was originally designed and intended for use with React. There are UI binding layers for many other frameworks, but React Redux is maintained directly by the Redux team.

As the offical Redux binding for React, React Redux is kept up-to-date with any API changes from either library, to ensure that your React components behave as expected. Its intended usage adopts the design principles of React - writing declarative components.

2. It Encourages Good React Architecture

The React Redux connect function generates "container" wrapper components that handle the process of interacting with the store for you. That way, your own components can focus on other tasks, whether it be collecting other data, or just displaying a piece of the UI. In addition, connect abstracts away the question of which store is being used, making your own components more reusable.

As a general architectural principle, we want to keep our own components "unaware" of Redux. They should simply receive data and functions as props, just like any other React component. This ultimately makes it easier to test and reuse your own components.

3. It Implements Performance Optimizations For You

 React Redux implements many performance optimizations internally, so that your own component only re-renders when it actually needs to.
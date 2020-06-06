# ReactJS

## What is react js

React is an open-source JavaScript library for building user interfaces. It is maintained by Facebook and a community of individual developers and companies.  

## Why to use react js

React can be used as a base in the development of single-page or mobile applications. However, React is only concerned with rendering data to the DOM, and so creating React applications usually requires the use of additional libraries for state management and routing. **`Redux`** and **`React Router`** are respective examples of such libraries.

## Pre requisits
- HTML  
- JavaScript / Typescript
    - arraw functions
    - classes
    - let
    - const 
    - etc.

## Notable features

### Components

Components are small and isolated pieces of code, that lets you compose complex UIs.

- **props** : props are inputs to a React component. They are data passed down from a parent component to a child component.
- **state** : special built-in object in React, which allows components to create and manage their own data. So unlike props, components cannot pass data with state, but they can create and manage it internally.

- #### Functional components

     Functional components are declared with a function that then returns some JSX

    ```javascript
    const Greeting = (props) => <div>Hello, {props.name}!</div>;
    ```

- #### Class-based components

    Class-based components are declared using ES6 classes. They are also known as "stateful" components, because their state can hold values throughout the component and can be passed to child components through props

    ```javascript
    class ParentComponent extends React.Component {
        state = { color: 'green' };
        render() {
            return (
            <ChildComponent color={this.state.color} />
            );
        }
    }
    ```

### Virtual DOM

The virtual DOM (VDOM) is a programming concept where an ideal, or “virtual”, representation of a UI is kept in memory and synced with the “real” DOM by a library such as ReactDOM. This process is called reconciliation.

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/BYbgopx44vo/0.jpg)](https://www.youtube.com/watch?v=BYbgopx44vo)   

### JSX

JSX is a syntax extension to JavaScript. It is similar to a template language, but it has full power of JavaScript. JSX gets compiled to `React.createElement()` calls which return plain JavaScript objects called `React elements` or `Components`.

- JSX

```javascript
class HelloMessage extends React.Component {
  render() {
    return (
      <div>
        Hello {this.props.name}
      </div>
    );
  }
}

ReactDOM.render(
  <HelloMessage name="Taylor" />,
  document.getElementById('hello-example')
);
```
- Javascript

```javascript
class HelloMessage extends React.Component {
  render() {
    return React.createElement(
      "div",
      null,
      "Hello ",
      this.props.name
    );
  }
}

ReactDOM.render(React.createElement(HelloMessage, { name: "Taylor" }), document.getElementById('hello-example'));
```

### React Component Lifecycle

Lifecycle methods are custom functionality that gets executed during the different phases of a component. There are methods available when the component gets created and inserted into the DOM (mounting), when the component updates, and when the component gets unmounted or removed from the DOM.

### React Hooks

A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components.

**When to use a Hook?** If you write a `function component` and realize you need `to add some state` to it, previously you had to convert it to a class. Now you can use a Hook inside the existing function component.




# First Application

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

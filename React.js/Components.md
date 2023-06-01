# Components

In React, everything is a component. A component is a reusable piece of code that encapsulates state and behavior. Components can be used to create complex user interfaces from simple, reusable building blocks.

#### Class Components

Class components are the original way to write React components. They are based on the concept of classes in JavaScript. Class components have a state property, which is used to store data that can change over time. They also have a render method, which is used to generate the HTML output for the component.

Here is an example of a class component:

```js
class MyComponent extends React.Component {
  state = {
    count: 0
  };

  incrementCount = () => {
    this.setState({
      count: this.state.count + 1
    });
  };

  render() {
    return (
      <div>
        <h1>My Component</h1>
        <p>The count is {this.state.count}</p>
        <button onClick={this.incrementCount}>Increment Count</button>
      </div>
    );
  }
}

```

This component has a state property that stores the current count. It also has a render method that generates the HTML output for the component. The incrementCount method increments the count and updates the state.



#### Functional Components

Functional components are a newer way to write React components. They are based on the concept of functions in JavaScript. Functional components do not have a state property or a render method. Instead, they use the useState and useEffect hooks to manage state and side effects.

Here is an example of a functional component:

```js
const MyComponent = () => {
  const [count, setCount] = useState(0);

  const incrementCount = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <h1>My Component</h1>
      <p>The count is {count}</p>
      <button onClick={incrementCount}>Increment Count</button>
    </div>
  );
};

```

This component uses the useState hook to manage the count state. The useEffect hook is used to update the count when the component is mounted or unmounted.

#### Hooks

Hooks are a new feature in React 16.8 that allow you to use state and other React features without writing a class component. Hooks are functions that you can use to access state, lifecycle methods, and other React features from functional components.

Here is an example of how to use the useState hook:

```js
const MyComponent = () => {
  const [count, setCount] = useState(0);
  return (
    <div>
      <h1>My Component</h1>
      <p>The count is {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment Count</button>
    </div>
  );
};
```

This component uses the useState hook to manage the count state. The useState hook returns an array with two values: the current state value and a function that can be used to update the state.

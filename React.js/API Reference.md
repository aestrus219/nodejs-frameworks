# API Reference

The API Reference is a comprehensive guide to all of the APIs provided by React.js. It includes documentation for all of the React components, functions, and classes, as well as the ReactDOM and React Router APIs.

#### React API Reference

The React API Reference provides documentation for all of the React components, functions, and classes. It includes information on how to use each API, as well as examples of how to use them in code.

Here is an example of a React component:

```js
class MyComponent extends React.Component {
  render() {
    return (
      <div>
        <h1>Hello, world!</h1>
      </div>
    );
  }
}
```

This component renders a simple "Hello, world!" message.

#### ReactDOM API Reference

The ReactDOM API Reference provides documentation for the ReactDOM library, which is used to render React components to the DOM. It includes information on how to use ReactDOM to render components, as well as examples of how to do so.

Here is an example of how to render a React component using ReactDOM:

```js
ReactDOM.render(<MyComponent />, document.getElementById("root"));
```

This code renders the `MyComponent` component to the element with the ID `root`.

#### React Router API Reference

The React Router API Reference provides documentation for the React Router library, which is used to manage routing in React applications. It includes information on how to use React Router to create routes, as well as examples of how to do so.

Here is an example of how to create a route using React Router:

```js
const routes = [
  {
    path: "/",
    component: Home,
  },
  {
    path: "/about",
    component: About,
  },
];

const App = () => {
  return (
    <Router routes={routes} />
  );
};
```

This code creates two routes: one for the `/` path, which renders the `Home` component, and one for the `/about` path, which renders the `About` component.

#### React Hooks API Reference

The React Hooks API Reference provides documentation for the React Hooks API, which is a new way to use React that allows you to use state and other React features without having to write a class. It includes information on how to use each hook, as well as examples of how to use them in code.

Here is an example of how to use the `useState` hook to create a counter:

```js
const [count, setCount] = useState(0);

const increment = () => {
  setCount(count + 1);
};

const decrement = () => {
  setCount(count - 1);
};

const App = () => {
  return (
    <div>
      <h1>Count: {count}</h1>
      <button onClick={increment}>Increment</button>
      <button onClick={decrement}>Decrement</button>
    </div>
  );
};
```

This code creates a counter that can be incremented and decremented.



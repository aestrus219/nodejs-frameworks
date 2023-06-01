# Getting Started

#### Hello World

The first thing you'll want to do is create a new React application. You can do this by using the `create-react-app` command-line tool. Once you've created your application, you'll be able to start it by running the `npm start` command. This will start a development server on port 3000. You can then open your browser and go to `http://localhost:3000` to see your application.

The default `create-react-app` application will display the following text:

```
Welcome to React!
```

This is a simple example of a React application. It doesn't do anything, but it shows you how to create a basic React application.

#### Introducing JSX

React uses a special syntax called JSX to render HTML elements. JSX looks like HTML, but it's actually JavaScript. This allows you to combine your JavaScript code with your HTML code, which makes it easier to create complex user interfaces.

Here's an example of how to use JSX to render a simple button:

```js
const App = () => {
  return (
    <button>Click Me</button>
  );
};
```

This code will render a button with the text "Click Me".

#### Rendering Elements

You can use the `React.createElement()` function to render React elements. The `React.createElement()` function takes two arguments: the first argument is the name of the element you want to render, and the second argument is an object containing the element's properties.

Here's an example of how to use `React.createElement()` to render a paragraph element with the text "This is a paragraph":

```js
const App = () => {
  return (
    <p>This is a paragraph</p>
  );
};
```

#### Components and Propsjs

React components are reusable pieces of code that can be used to create complex user interfaces. Components are defined using the `const` keyword.

Here's an example of a simple component:

```js
const MyComponent = () => {
  return (
    <div>This is a component</div>
  );
};
```

You can use components by passing them as props to other components. Props are simply JavaScript objects that can be used to pass data to components.

Here's an example of how to use a component as a prop:

```js
const App = () => {
  return (
    <MyComponent />
  );
};
```

#### State and Lifecycle

React components have a state object that can be used to store data that changes over time. The state object is updated using the `setState()` method.

The React lifecycle is a series of events that are triggered when a component is created, mounted, updated, and unmounted. You can use the lifecycle methods to perform specific tasks at specific times in the component's lifecycle.

##### Handling Events

React components can handle events by using the `on` event handler. The `on` event handler takes two arguments: the first argument is the name of the event, and the second argument is a function that will be called when the event is triggered.

Here's an example of how to handle a click event:

```js
const MyComponent = () => {
  return (
    <div onClick={() => {
      alert("You clicked me!");
    }}>
      Click me!
    </div>
  );
};
```

#### Conditional Rendering

React components can render different HTML depending on the value of a variable. This is done using the `if` statement.

Here's an example of how to use `if` to render different HTML depending on the value of a variable:

```js
const MyComponent = () => {
  const isLoggedIn = true;
  if (isLoggedIn) {
    return (
      <div>You are logged in!</div>
    );
  } else {
    return (
      <div>You are not logged in!</div>
    );
  }
};
```

#### Lists and Keys

React components can render lists of elements using the `map()` function. The `map()` function takes two arguments: the first argument is an array of elements, and the second argument is a function that will be called for each element in the array.

Here's an example of how to use `map()` to render a list of items:

```js
const MyComponent = () => {
      const items = ['Item 1', 'Item 2', 'Item 3'];

      return (
        <ul>
          {items.map((item) => (
            <li key={item}>{item}</li>
          ))}
        </ul>
      );
    };
```

The `key` prop is used to identify each element in the list. This is important for React to be able to track changes to the list and update the DOM accordingly.

#### Forms

React components can be used to create forms. Forms are created using the `Form` component. The `Form` component takes two arguments: the first argument is the name of the form, and the second argument is an object containing the form's properties.

Here's an example of how to create a form:

```js
const MyComponent = () => {
  const form = new Form('my-form');
  return (
    <form onSubmit={form.submit}>
      <input name="name" />
      <input type="submit" value="Submit" />
    </form>
  );
};
```

The `onSubmit` event handler is called when the form is submitted. This event handler can be used to process the form data.

#### Lifting State Up

When a component needs to share state with its children, it can use the `LiftStateUp` component. The `LiftStateUp` component takes two arguments: the first argument is the name of the state variable, and the second argument is the value of the state variable.

Here's an example of how to use `LiftStateUp` to share state with children:

```js
const MyComponent = () => {
  const [count, setCount] = useState(0);

  return (
    <div>
      <h1>Count: {count}</h1>
      <MyChild />
    </div>
  );
};

const MyChild = () => {
  const [count, setCount] = useState(0);

  return (
    <div>
      <h2>Child Count: {count}</h2>
      <button onClick={() => {
        setCount(count + 1);
      }}>Increment</button>
    </div>
  );
};
```

In this example, the `MyComponent` component has a state variable called `count`. The `MyChild` component uses the `LiftStateUp` component to share the `count` state variable with its children.

#### Composition vs Inheritance

In React, there are two ways to create components: composition and inheritance. Composition is the preferred way to create components. Inheritance should only be used when it is absolutely necessary.

Composition is the process of combining existing components to create new components. This allows you to create complex components without having to write a lot of code.

Inheritance is the process of creating a new component that inherits from an existing component. This allows you to reuse code from existing components.

#### Thinking In React

When you're thinking in React, you need to think about the components that make up your application. You need to think about how the components interact with each other. You also need to think about how the components will be rendered to the DOM.

If you can think in React, you'll be able to create complex applications that are easy to maintain and update.



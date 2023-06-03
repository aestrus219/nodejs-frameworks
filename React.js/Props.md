# Props

Props are arguments that are passed into React components. They are used to pass data from one component to another. Props are always passed as an object, and each property in the object represents a single prop.

For example, the following code passes a prop called `name` to the `Hello` component:

```js
<Hello name="John Doe" />
```

The `Hello` component can then access the `name` prop using the `this.props.name` property.

#### Passing Props

Props can be passed to components in a number of ways. They can be passed directly as attributes on the component tag, or they can be passed indirectly via a higher-order component.

To pass props directly as attributes, simply add the prop name and value to the component tag. For example:

```js
<Hello name="John Doe" />
```

To pass props indirectly via a higher-order component, use the `withProps` higher-order component. For example:

```js
const withName = props => {
  return (
    <Hello name={props.name} />
  );
};
const App = () => {
  return (
    <withName name="John Doe" />
  );
};
```

#### Default Props

If you want to provide a default value for a prop, you can do so by defining the prop in the component's definition. For example:

```js
const Hello = ({ name = "John Doe" }) => {
  return (
    <div>Hello, {name}</div>
  );
};
```

In this example, the `name` prop has a default value of "John Doe". If no value is passed for `name`, the component will use the default value.

#### Prop Types

Prop types are used to validate the types of props that are passed to a component. Prop types can be defined using the `PropTypes` object. For example:

```js
const Hello = ({ name: string }) => {
  return (
    <div>Hello, {name}</div>
  );
};
```

In this example, the `name` prop is required to be a string. If a non-string value is passed for `name`, an error will be thrown.

#### Prop Validation

Prop validation is used to ensure that the props that are passed to a component are valid. Prop validation can be done using the `validateProps` function. For example:

```js
const Hello = ({ name: string }) => {
  return (
    <div>Hello, {name}</div>
  );
};

const validateProps = props => {
  if (!props.name) {
    throw new Error("The name prop is required");
  }

  return props;
};

const App = () => {
  return (
    <Hello name="John Doe" />
  );
};
```

In this example, the `validateProps` function ensures that the `name` prop is not empty. If the `name` prop is empty, an error will be thrown.

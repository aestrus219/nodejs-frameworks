# Rendering

Rendering is the process of creating a visual representation of a React component. It is done by calling the `render()` method on the component. The `render()` method returns a React element, which is a description of the desired output.

For example, the following code renders a simple `div` element:

```js
const Hello = () => {
  return (
    <div>Hello, world!</div>
  );
};
```

The `render()` method in this example returns a single `div` element with the text "Hello, world!".

#### JSX

JSX is a syntax extension for JavaScript that allows you to write React elements. JSX looks like HTML, but it is actually JavaScript code.

For example, the following code is equivalent to the previous example:

```js
const Hello = () => {
  return <div>Hello, world!</div>;
};
```

#### Conditional Rendering

Conditional rendering is the ability to render different output depending on the value of a prop or state variable.

For example, the following code renders a different message depending on whether the `isLoggedIn` prop is true or false:

```js
const Hello = ({ isLoggedIn }) => {
  if (isLoggedIn) {
    return <div>Hello, logged in user!</div>;
  } else {
    return <div>Hello, guest!</div>;
  }
};
```

#### Lists and Keys

Lists are a way to render multiple elements at once. When rendering a list, it is important to use keys to identify each element. Keys are used to ensure that React can correctly update the DOM when the list changes.

For example, the following code renders a list of names:

```js
const Names = () => {
  const names = ["John", "Mary", "Peter"];
  return (
    <ul>
      {names.map((name, index) => (        <li key={index}>{name}</li>
      ))}    </ul>
  );
};
```

In this example, the `names` array is mapped to a list of `li` elements. Each `li` element has a key that is the index of the element in the array. This ensures that React can correctly update the DOM when the `names` array changes.

#### Formatting

React provides a number of ways to format the output of a component. These methods can be used to change the font, size, color, and other properties of the output.

For example, the following code changes the font size of the output:

```js
const Hello = () => {
  return (
    <div style={{ fontSize: "24px" }}>Hello, world!</div>
  );
};
```

#### Styling

React provides a number of ways to style the output of a component. These methods can be used to change the background color, border, margin, and other properties of the output.

For example, the following code changes the background color of the output:

```js
const Hello = () => {
  return (
    <div style={{ backgroundColor: "red" }}>Hello, world!</div>
  );
};
```



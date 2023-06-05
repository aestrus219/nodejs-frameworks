# Events

Events are actions that can be triggered by the user, such as a mouse click, a key press, or a change in the DOM. React provides a way to handle events in a consistent way across all browsers.

#### Handling Events

To handle an event, you can use the `onClick` prop. For example, the following code will handle a click event on the `button` element:

```js
<button onClick={() => alert('Hello!')}>Click me!</button>
```

The `onClick` prop takes a function as its value. This function will be called whenever the user clicks on the button.

#### Event Delegation

Event delegation is a technique that can be used to handle events on a large number of elements without having to attach event handlers to each individual element. To use event delegation, you can use the `on` prop. For example, the following code will handle a click event on any `li` element in the `ul` element:

```js
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>

<script>
function handleClick(e) {
  e.target.textContent = 'Clicked!';
}

const ul = document.querySelector('ul');
ul.on('click', handleClick);
</script>
```

The `on` prop takes an event name and a function as its values. The function will be called whenever an event of the specified type is triggered on the element.

#### Event Bubbling

Event bubbling is a process by which an event is propagated up the DOM tree. For example, if a user clicks on an `img` element, the `click` event will be first triggered on the `img` element, then on its parent element, and so on, until it reaches the root of the DOM tree.

You can use the `stopPropagation` method to prevent an event from bubbling up the DOM tree. For example, the following code will prevent the `click` event from bubbling up from the `img` element:

```js
<img onclick={() => alert('Hello!')} onmouseup={e => e.stopPropagation()} />
```

The `stopPropagation` method prevents the event from being propagated to any parent elements.

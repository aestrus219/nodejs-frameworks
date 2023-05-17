### Templates

#### Interpolation

In Vue.js, you can use interpolation to display data in your HTML templates. Interpolation is done using double curly braces `({{ }})`.
Here's an example:
```html
<div id="app">
  {{ message }}
</div>
```

This code displays the value of the `message` variable in the HTML template.

#### Directives

Vue.js provides several built-in directives that you can use to manipulate the DOM, handle events, and conditionally render elements.

Here are some examples:

-   `v-bind`: Binds an element's attribute to a data property. For example,  `v-bind:href="url"`  binds the  `href`  attribute to the  `url`  data property.
-   `v-if`: Conditionally renders an element based on a condition. For example,  `v-if="show"`  only renders the element if the  `show`  data property is true.
-   `v-for`: Renders a list of elements based on an array. For example,  `v-for="item in items"`  renders an element for each item in the  `items`  array.

Here's an example that uses the `v-for` directive to render a list of items:

```html
<ul>
  <li v-for="item in items">{{ item }}</li>
</ul>
```

This code renders an unordered list with a list item for each item in the `items` array.

#### Filters

Vue.js provides filters that you can use to format data in your templates. Filters are added to an expression using the pipe (`|`) symbol.

Here's an example:

```html
<div id="app">
  {{ message | capitalize }}
</div>
```

This code uses the `capitalize` filter to capitalize the `message` variable before displaying it in the HTML template.

To define a filter, you can use the `Vue.filter` method:

```javascript
Vue.filter('capitalize', function(value) {
  if (!value) return '';
  value = value.toString();
  return value.charAt(0).toUpperCase() + value.slice(1);
});
```

This code defines a `capitalize` filter that capitalizes the first letter of a string.
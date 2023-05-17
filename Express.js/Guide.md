### Guide

#### Routing

Routing is a way to define different pages and actions in your. In Express.js, you can use methods like `get`, `post`, `put`, and `delete` to handle different types of requests.

Here's an example of a route for a "Contact" page that uses the `post` method to handle form submissions:

```javascript
app.post('/contact', (req, res) => {
  const name = req.body.name;
  const email = req.body.email;
  const message = req.body.message;
  // Do something with the form data
  res.send('Thanks for contacting us!');
});
```

This code defines a route for the "Contact" page ("/contact") using the `post` method. When someone submits a form on the "Contact" page, the app receives the form data in the `req.body` object. In this example, we're extracting the name, email, and message fields from the form data and doing something with them. Finally, the app sends a "Thanks for contacting us!" message as a response.

#### Middleware

Middleware are functions that can do things before or after your app does something. In Express.js, middleware functions can be used to modify requests and responses, handle errors, and more.

Here's an example of a middleware function that logs the time of each request:

```javascript
const logger = (req, res, next) => {
  console.log(`[${new Date().toISOString()}] ${req.method} ${req.url}`);
  next();
};

app.use(logger);
```

This code defines a middleware function named "logger" that takes three arguments: `req` (the request object), `res` (the response object), and `next` (a function that tells Express.js to move on to the next middleware function). In this example, the logger function logs the current time, the HTTP method, and the URL of each request. The `app.use(logger)` line tells Express.js to use the "logger" middleware function for all requests.

#### Using template engines

Template engines help you generate HTML pages dynamically using data from your app. In Express.js, you can use template engines like EJS, Handlebars, and Pug.

Here's an example of an EJS template that displays a list of items:

```html
<ul>
  <% items.forEach((item) => { %>
    <li><%= item %></li>
  <% }); %>
</ul>
```

This code defines an unordered list in HTML and uses EJS syntax to loop through an array of items and generate an HTML list item for each item.

To use this template in your Express.js app, you need to set the view engine to EJS and render the template with data from your app. Here's an example:

```javascript
app.set('view engine', 'ejs');

app.get('/items', (req, res) => {
  const items = ['apple', 'banana', 'orange'];
  res.render('items', { items: items });
});
```

This code sets the view engine to EJS and defines a route for an "Items" page ("/items") using the `get` method. In this example, we're generating a list of items and passing it to the "items" template using the `res.render` method. The `items` variable is passed to the template as an object property.
### Advanced Topics

#### Middleware

Middleware functions are functions that have access to the request and response objects, and the next middleware function in the application's request-response cycle. Middleware functions can be used to modify requests and responses, handle errors, and more.

Here's an example of a middleware function that logs the time of each request:

```javascript
const logger = (req, res, next) => {
  console.log(`[${new Date().toISOString()}] ${req.method} ${req.url}`);
  next();
};

app.use(logger);
```

This code defines a middleware function named "logger" that takes three arguments: `req` (the request object), `res` (the response object), and `next` (a function that tells Express.js to move on to the next middleware function). In this example, the logger function logs the current time, the HTTP method, and the URL of each request. The `app.use(logger)` line tells Express.js to use the "logger" middleware function for all requests.

#### Error handling

Express.js provides a way to handle errors using middleware functions. Here's an example of an error handling middleware function:

```javascript
app.use((err, req, res, next) => {
  console.error(err.stack);
  res.status(500).send('Something broke!');
});
```

This code defines an error handling middleware function that takes four arguments: `err` (the error object), `req` (the request object), `res` (the response object), and `next` (a function that tells Express.js to move on to the next middleware function). In this example, the error handling function logs the error stack trace to the console and sends a "Something broke!" message as a response with a 500 status code.

#### Routing

Routing is a way to define different pages and actions in your app. In Express.js, you can use methods like `get`, `post`, `put`, and `delete` to handle different types of requests.

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

#### Template engines

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
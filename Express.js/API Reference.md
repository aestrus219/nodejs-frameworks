### API Reference

The Express.js API reference provides a comprehensive list of all the methods and properties available in the Express.js framework. Here are some examples of commonly used methods and properties:

#### `app.get()`

The `app.get()` method is used to define a route for handling GET requests. Here's an example:

```javascript
app.get('/users', (req, res) => {
  // Handle GET request for /users
});
```

This code defines a route for handling GET requests to the "/users" URL. When a user visits the "/users" URL, the app executes the callback function and sends a response.

#### `app.post()`

The `app.post()` method is used to define a route for handling POST requests. Here's an example:

```javascript
app.post('/users', (req, res) => {
  // Handle POST request for /users
});
```

This code defines a route for handling POST requests to the "/users" URL. When a user submits a form to the "/users" URL, the app executes the callback function and sends a response.

#### `req.params`

The `req.params` property is an object containing properties mapped to the named route “parameters”. Here's an example:

```javascript
app.get('/users/:id', (req, res) => {
  const userId = req.params.id;
  // Handle GET request for /users/:id
});
```

This code defines a route for handling GET requests to the `/users/:id` URL. When a user visits a URL like `/users/123`, the app extracts the value `123` from the URL and stores it in the `req.params` object. In this example, we're extracting the `id` parameter from the URL and using it to handle the request.

#### `res.send()`

The `res.send()` method is used to send a response to the client. Here's an example:

```javascript
app.get('/users', (req, res) => {
  res.send('Hello, World!');
});
```

This code defines a route for handling GET requests to the "/users" URL. When a user visits the "/users" URL, the app sends the string "Hello, World!" as a response.

#### `res.json()`

The `res.json()` method is used to send a JSON response to the client. Here's an example:

```javascript
app.get('/users', (req, res) => {
  const users = [{ name: 'John', age: 30 }, { name: 'Jane', age: 25 }];
  res.json(users);
});
```

This code defines a route for handling GET requests to the "/users" URL. When a user visits the "/users" URL, the app sends a JSON response containing an array of user objects.
### Getting Started

#### Installation

To use Express.js, you need to install it on your computer. You can do this using the Node.js package manager (npm) by running the following command in your terminal or command prompt:

```bash
npm install express
```

This command installs the Express.js package and makes it available for use in your project.

#### Hello World example

The following code creates a simple Express.js app that responds with "Hello, World!" when you visit the main page:

```javascript
const express = require('express');
const app = express();
const port = 3000;

app.get('/', (req, res) => {
  res.send('Hello, World!');
});

app.listen(port, () => {
  console.log(`App listening at http://localhost:${port}`);
});
```

This code does the following:

1. Imports the Express.js package and creates a new Express.js app.
2. Defines a route for the main page ("/") using the `get` method. When someone visits the main page, the app sends "Hello, World!" as a response.
3. Starts the app listening on port 3000 and logs a message to the console.

#### Basic routing

The following code defines a route for an "About" page:

```javascript
app.get('/about', (req, res) => {
  res.send('About page');
});
```

This code defines a route for the "About" page ("/about") using the `get` method. When someone visits the "About" page, the app sends "About page" as a response.

#### Static files

The following code tells Express.js to serve static files from a folder named "public":

```javascript
app.use(express.static('public'));
```

This code tells Express.js to serve static files from a folder named "public". When someone requests a file, Express.js looks for it in the "public" folder and sends it as a response.
# Core Concepts

#### Data binding

Data binding is the process of connecting data from the model to the view. AngularJS provides two-way data binding, which means that changes to the model are automatically reflected in the view, and vice versa.

Here is an example of data binding:

```html
<input type="text" ng-model="name">
```

In this example, the value of the `name` input is bound to the `name` variable in the controller. When the user types in the input, the value of the `name` variable is updated. And when the value of the `name` variable is updated, the text in the input is updated.

#### Expressions

Expressions are JavaScript code that can be used to evaluate values and perform actions. Expressions can be used in data bindings, directives, and filters.

Here is an example of an expression:

```js
{{ name | uppercase }}
```

In this example, the `name` variable is evaluated and the result is converted to uppercase. The result is then displayed in the view.

#### Interpolation

Interpolation is a way to insert expressions into the HTML of a view. Interpolation is used to display the results of expressions in the view.

Here is an example of interpolation:

```html
<h1>Welcome, {{ name }}</h1>
```

In this example, the `name` variable is interpolated into the HTML of the `h1` tag. The result is a heading that says "Welcome, [name]."

#### Directives

Directives are custom HTML attributes that can be used to add functionality to the view. Directives can be used to create custom components, add validation, and more.

Here is an example of a directive:

```js
app.directive('myDirective', function() {
  return {
    link: function(scope, element, attrs) {
      // Do something when the directive is used
    }
  };
});
```

In this example, the `myDirective` directive is defined. The directive has a `link` function that is called when the directive is used. The `link` function can be used to add functionality to the view.

#### Views and routes

Views are the individual pages of an AngularJS application. Routes are used to navigate between views.

Here is an example of a route:

```js
app.config(['$routeProvider', function($routeProvider) {
  $routeProvider.when('/', {
    templateUrl: 'home.html'
  });
  $routeProvider.when('/about', {
    templateUrl: 'about.html'
  });
});
```

In this example, two routes are defined: `/` and `/about`. The `/` route is associated with the `home.html` template, and the `/about` route is associated with the `about.html` template.

#### Filters

Filters are functions that can be used to format data. Filters can be used to convert values to different formats, apply conditional logic, and more.

Here is an example of a filter:

```js
app.filter('uppercase', function() {
  return function(value) {
    return value.toUpperCase();
  };
});
```

In this example, the `uppercase` filter is defined. The `uppercase` filter can be used to convert a value to uppercase.

#### HTML compiler

The HTML compiler is responsible for compiling AngularJS templates into JavaScript code. The HTML compiler is used to create a dependency graph between the different components of an AngularJS application.

#### Forms

Forms are used to collect user input. AngularJS provides a number of features for working with forms, such as validation, data binding, and custom controls.

Here is an example of a form:

```js
<form ng-submit="submit()">
  <input type="text" ng-model="name">
  <button type="submit">Submit</button>
</form>
```

In this example, a form is created with an input field and a submit button. The `name` variable is bound to the input field. When the user clicks on the submit button, the `submit()` function in the controller is called.

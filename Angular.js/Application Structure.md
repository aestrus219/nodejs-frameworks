# Application Structure

#### Modules

AngularJS applications are organized into modules. A module is a collection of AngularJS code that defines a set of related functionality. Modules are loaded and unloaded dynamically, which makes AngularJS applications more flexible and scalable.

To create a module, you need to create a file with the .js extension and add the following code to it:

```js
angular.module('myApp', []);
```

The `angular.module()` function takes two arguments: the name of the module and an array of dependencies. The name of the module is used to refer to the module in your code. The dependencies are other modules that the current module needs to function.

> Once you have created a module, you can start adding controllers, services, and other AngularJS code to it.

#### Controllers

Controllers are AngularJS objects that control the behavior of a portion of your application. Controllers are responsible for handling user input, updating the DOM, and communicating with services.

To create a controller, you need to create a JavaScript function with the `controller()` function. The `controller()` function takes two arguments: the name of the controller and an object that contains the controller's properties and methods.

The following code creates a controller named `MyController`:

```js
app.controller('MyController', function($scope) {
  $scope.message = 'Hello, world!';
});
```

The `$scope` object is an AngularJS object that provides access to the current scope. The `message` property on the `$scope` object is used to store the message that will be displayed to the user.

#### Services

Services are AngularJS objects that provide reusable functionality. Services can be used to perform tasks such as accessing data from a server, validating user input, and formatting data.

To create a service, you need to create a JavaScript function with the `service()` function. The `service()` function takes two arguments: the name of the service and an object that contains the service's properties and methods.

The following code creates a service named `MyService`:

```js
app.service('MyService', function($http) {
  this.getData = function() {
    return $http.get('/data');
  };
});
```

The `$http` object is an AngularJS object that provides access to the HTTP service. The `getData()` method on the `MyService` object is used to get data from the server.

#### Factories

Factories are AngularJS objects that are used to create other AngularJS objects. Factories are often used to create services.

To create a factory, you need to create a JavaScript function with the `factory()` function. The `factory()` function takes two arguments: the name of the factory and an object that contains the factory's properties and methods.

The following code creates a factory named `MyFactory`:

```js
app.factory('MyFactory', function($http) {
  function MyService() {
    // ...
  }
  return MyService;
});
```

The `$http` object is an AngularJS object that provides access to the HTTP service. The `MyService` function is used to create a `MyService` object.

#### Providers

Providers are AngularJS objects that provide configuration and dependency injection services. Providers are often used to configure services and to inject dependencies into controllers.

To create a provider, you need to create a JavaScript function with the `provider()` function. The `provider()` function takes three arguments: the name of the provider, an object that contains the provider's properties, and a function that is used to initialize the provider.

The following code creates a provider named `MyProvider`:

```js
app.provider('MyProvider', function() {
  this.myProperty = 'Hello, world!';

  function MyInitializer() {
    // ...
  }

  this.initialize = MyInitializer;
});
```

The `myProperty` property on the `MyProvider` object is used to store a message that will be displayed to the user. The `MyInitializer` function is used to initialize the `MyProvider` object.

#### Scopes

Scopes are AngularJS objects that are used to store data and to define the behavior of directives. Scopes are created by controllers and are passed down to directives.

Scopes have a number of properties and methods that can be used to store data, to define the behavior of directives, and to communicate with other scopes.

#### Dependency Injection

Dependency injection is a design pattern that allows you to decouple the code that needs a dependency from the code that provides the dependency. This makes your code more flexible and easier to test.

To use dependency injection in AngularJS, you need to use the `inject` annotation. The `inject` annotation tells AngularJS how to inject a dependency into a controller or service.

The following code shows how to use the `inject` annotation to inject a service into a controller:

```js
app.controller('MyController', function($scope, MyService) {
  // ...
});
```

The `MyService` parameter is a dependency that is injected into the `MyController` controller.

Dependency injection is a powerful tool that can help you to write more flexible and easier to test AngularJS applications.

Here is a summary of the benefits of using dependency injection in AngularJS:

* **Flexibility:** Dependency injection makes your code more flexible because it allows you to change the implementation of a dependency without having to change the code that uses the dependency.
* **Easier testing:** Dependency injection makes your code easier to test because it allows you to mock or stub out dependencies in your unit tests.
* **Reusability:** Dependency injection makes your code more reusable because it allows you to create reusable components that can be injected into other applications.

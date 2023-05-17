### Vue Router

Vue Router is the official router for Vue.js. It allows you to build single-page applications with multiple views and URLs.

#### Installation

To install Vue Router you can run the following command in your terminal or command prompt:

```bash
npm install vue-router
```

or via yarn:

```bash
yarn add vue-router
```

#### Basic usage

To use Vue Router in your Vue.js application, you need to create a router instance and define your routes:

```javascript
import Vue from 'vue';
import VueRouter from 'vue-router';

Vue.use(VueRouter);

const routes = [
  { path: '/', component: Home },
  { path: '/about', component: About },
  { path: '/contact', component: Contact }
];

const router = new VueRouter({
  routes
});

const app = new Vue({
  router
}).$mount('#app');
```

This code creates a new router instance with three routes: `/`, `/about`, and `/contact`. Each route is associated with a component.

To display the router's views in your HTML template, you can use the `router-view` component:

```html
<div id="app">
  <router-view></router-view>
</div>
```

This code displays the router's views inside the `#app` element.

#### Navigation

To navigate between routes in your Vue.js application, you can use the `router-link` component:

```html
<router-link to="/">Home</router-link>
<router-link to="/about">About</router-link>
<router-link to="/contact">Contact</router-link>
```

This code creates three links that navigate to the `/`, `/about`, and `/contact` routes.

You can also navigate programmatically using the `$router` object:

```javascript
this.$router.push('/about');
```

This code navigates to the `/about` route.

#### Route parameters

Vue Router allows you to define dynamic routes with parameters. To define a route with a parameter, you can use a colon (`:`) followed by the parameter name:

```javascript
const routes = [
  { path: '/user/:id', component: User }
];
```

This code defines a route with a `id` parameter.

To access the parameter in your component, you can use the `$route` object:

```javascript
export default {
  mounted() {
    console.log(this.$route.params.id);
  }
}
```

This code logs the ~ parameter to the console.

#### Nested routes

Vue Router allows you to define nested routes, where a route's component contains its own router-view:

```javascript
const routes = [
  {
    path: '/user/:id',
    component: User,
    children: [
      { path: 'profile', component: Profile },
      { path: 'settings', component: Settings }
    ]
  }
];
```

This code defines a route with a `User` component that contains two nested routes: `/user/:id/profile` and `/user/:id/settings`.

To display the nested routes in your HTML template, you can use the nested `router-view` components:

```html
<router-view></router-view>
<router-view name="profile"></router-view>
<router-view name="settings"></router-view>
```

This code displays the `User` component's view and the nested `Profile` and `Settings` components' views.
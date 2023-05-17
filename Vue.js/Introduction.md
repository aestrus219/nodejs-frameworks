# Introduction

#### What is Vue.js?

Vue.js is a progressive JavaScript framework for building user interfaces. It was created by Evan You and first released in 2014. Vue.js is designed to be easy to use and understand, with a focus on simplicity and flexibility.

#### Why use Vue.js?

Vue.js has several advantages over other JavaScript frameworks:

-   **Easy to learn:** Vue.js has a gentle learning curve and can be easily integrated into existing projects.
-   **Lightweight:** Vue.js is a lightweight framework, with a small file size and fast performance.
-   **Flexible:** Vue.js can be used for building small to large-scale applications, and can be easily integrated with other libraries and frameworks.
-   **Reactive:** Vue.js uses a reactive data binding system, which makes it easy to build dynamic and responsive user interfaces.

#### Getting started
##### Installation
- **CDN**
To get started with Vue.js, you can include the Vue.js library in your HTML file using a script tag:
```html
<script src="https://cdn.jsdelivr.net/npm/vue"></script>
```
- **NPM**
To install Vue.js using npm, you can run the following command in your terminal or command prompt:
```bash
npm install vue
```
- **Yarn**
To install Vue.js using yarn, you can run the following command:
```bash
yarn add vue
```
##### Usage
Once you've installed Vue.js, you can create a new Vue instance:
```javascript
import Vue from 'vue';

const app = new Vue({
  el: '#app',
  data: {
    message: 'Hello, Vue!'
  }
});
```
---
> **Note:** You don't need to import vue when adding it via CDN in your project.
---
This will create a new Vue instance and bind it to an element with the ID "app". The `data` property defines a message variable that can be used in the HTML template. In this example, the message variable is set to "Hello, Vue!".

To use the message variable in the HTML template, you can use the double curly brace syntax:
```html
<div id="app">
  {{ message }}
</div>
```
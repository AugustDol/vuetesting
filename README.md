# Vue.js Learning Demo

This project is a simple Vue.js application designed as a learning demo for Vue.js beginners.

key terms:

**The DOM** (Document Object Model) is a programming interface for HTML and XML documents. It represents the structure of a document as a tree-like model, where each node represents an element, attribute, or piece of text in the document.

With **the DOM**, you can manipulate the content and structure of a web page dynamically. You can access and modify elements, add or remove nodes, change styles and attributes, and handle events.

Here is an example of how to access an element using the DOM:

```javascript
// Access an element by its ID
var element = document.getElementById("myElement");

// Access elements by their class name
var elements = document.getElementsByClassName("myClass");

// Access elements by their tag name
var elements = document.getElementsByTagName("p");
```

## Text Interpolation

In Vue.js, you can use the double curly braces `{{ }}` to display data from your Vue instance in your HTML. This is called text interpolation.

Here is an example of how to use text interpolation:

html:
```html
<div id="app">
  <p>{{ message }}</p>
</div>
```
js:
```js
const app = Vue.createApp({
  data() {
    return {
      message: "Hello, Vue!"
    }
  }
})
```

app.mount('#app')

## v-bind Directive
The `v-bind` directive is used in Vue.js to bind an attribute of an HTML element to an expression. It dynamically updates the attribute whenever the value of the expression changes.

Here is an example of how to use the `v-bind` directive:

html:
```html
<div id="app">
  <div v-bind:class="vueClass"></div>
</div>
```

js:
```javascript
const app = Vue.createApp({
  data() {
    return {
      vueClass: "pinkBG"
    }
  }
})

app.mount('#app')
```

css:
```css
.pinkBG {
    background-color: lightpink;
}
```

## v-if Directive

The `v-if` directive is used to conditionally render a block of HTML based on the value of an expression. It works by evaluating the expression and only rendering the block if the expression evaluates to true.

Here is an example of how to use the `v-if` directive:

html:
```html
<div v-if="showMessage">
    <p>This message will only be shown if showMessage is true.</p>
</div>
```
js:
```javascript
const app = Vue.createApp({
  data() {
    return {
      showMessage: true //here if showMessage would've been false the block won't be visible
    }
  }
})
```

## v-show Directive

The `v-show` directive is really similar to the `v-if` directive but the key difference is that v-if destroys the element and it's children from the DOM, while `v-show` simply hides them by using CSS (`display: none`)

Here is an example of how to use the `v-show` directive:

html:
```html
    <div id="app">
        <h1 v-show="show">Hello World</h1>
        <button v-on:click="toggle">Toggle</button>
        
    </div>
```
js:
```js
  new Vue({
            el: '#app',
            data: {
                show: true
            },
            methods: {
                toggle() {
                    this.show = !this.show;
                }
            }
        });
```

## more comming soon...

to see where i left off click 
[HERE](https://www.w3schools.com/vue/vue_v-show.php).

:)


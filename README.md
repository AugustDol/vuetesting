# Vue.js Learning Demo

This project is a simple Vue.js application designed as a learning demo for Vue.js beginners.

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
```html
<div v-if="showMessage">
    <p>This message will only be shown if showMessage is true.</p>
</div>
```
```javascript
const app = Vue.createApp({
  data() {
    return {
      showMessage: true //here if showMessage would've been false the block won't be visible
    }
  }
})
```


## more comming soon...

to see where i left off click 
[HERE](https://www.w3schools.com/vue/vue_v-show.php).

:)


# Vue.js

> v2

### Including Vue

```html
<script src="https://unpkg.com/vue@2.5.16/dist/vue.js"></script>
```

### Using

```html
<div id="app">
  {{ message }}
</div>
```

```js
var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }
})
```

Output will be:
> Hello Vue!

### Good to know

- `v-on:blabla` is equal to `@blabla`
- `v-bind:blabla` is equal to `:blabla`

### Methods

```html
<div id="app">
  <button @click="foo">Click me</button>
</div>
```

```js
var app = new Vue({
  el: '#app',
  methods: {
    foo: function() {
      // Blabla
    }
  }
})
```

### Class
```html
<div :class="[isActive ? activeClass : '', errorClass]"></div>
```

---

```html
<div :class="[{active: isActive}, errorClass]"></div>
```

---

```html
<div class="blabla" :class="{active: isActive, 'text-danger': hasError}"></div>
```

```js
data: {
  isActive: true,
  hasError: false
}
```

It will render as:
```html
<div class="blabla active"></div>
```
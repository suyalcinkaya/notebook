# Vue.js

> v2

### Including Vue

```html
<script src="https://unpkg.com/vue@2.5.16/dist/vue.js"></script>
```
or
```html
<script src="https://unpkg.com/vue@2.5.16/dist/vue.min.js"></script>
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

## Useful Links
- Videos
    - English
        - [Vue.js Todo App](https://www.youtube.com/playlist?list=PLEhEHUEU3x5q-xB1On4CsLPts0-rZ9oos)
        - [Vue JS 2 Tutorial](https://www.youtube.com/playlist?list=PL4cUxeGkcC9gQcYgjhBoeQH7wiAyZNrYa)
        - [Learn Vue 2: Step By Step](https://www.youtube.com/playlist?list=PL3VM-unCzF8iRyPotjFsgy7EfuCITvr_3)
        - [Vue.js 2 - Getting Started](https://www.youtube.com/playlist?list=PL55RiY5tL51p-YU-Uw90qQH419BM4Iz07)
        - [Vue.js 2.0 In 60 Minutes](https://www.youtube.com/watch?v=z6hQqgvGI4Y&t=1s)
    - Turkish
        - [VueJS Türkçe Eğitim Videoları](https://www.youtube.com/playlist?list=PLa3NvhdFWNipwk1KXeUpVQnAiAfuBw4El)
        - [VueJS, Vue Router, Vuex, Firebase SPA Egitim Serisi](https://www.youtube.com/playlist?list=PLa3NvhdFWNirpx6x-LIMfTrwOfLzCkfAU)
        - [VueJS Eğitim Serisi](https://www.youtube.com/playlist?list=PLsGvMLC84GeTJeNRPH5P4w_S7tHSviLf6)
- Articles
    - English
        - [VueJS API](https://vuejs.org/v2/api)
        - [Passing methods as props in Vue.js](https://medium.com/front-end-hacking/passing-methods-as-props-in-vue-js-d65805bccee)
        - [Getting Started with Vue.js](https://sabe.io/tutorials/getting-started-with-vue-js)
    - Turkish 
- Books
    - English
    - Turkish

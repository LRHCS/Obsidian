reactive() and ref()

v-bind: id or :id/ :class

-   <div :id="dynamicId"></div>

Mouse Event

-   <button @click="increment">{{ count }}</button>

```jsx
<script setup>
import { ref } from 'vue'

const count = ref(0)

function increment() {
// update component state
count.value++
}
</script>
```

-   main.js(starter file)

```jsx
import { createApp } from "vue";
// import the root component App from a single-file component.
import App from "./App.vue";

const app = createApp(App);
app.mount("#app");
```

```jsx
<script setup>
import { ref, reactive } from 'vue'

const author = reactive({
     name: 'John Doe',
     books: [
          'Vue 2 - Advanced Guide',
          'Vue 3 - Basic Guide',
          'Vue 4 - The Mystery'
     ]
})
</script>

<template>
     <h1>{{ author.name }}</h1>
     <li v-for="(book, index) in author.books" v-if="author.books.length > 0" class="color">{{ index }} - {{ book }}</li>
     <p v-else>He/She has not published any books yet</p>
</template>

<style>
.color {
     color : black
}
.color:hover{
     color: red;
}
</style>
```
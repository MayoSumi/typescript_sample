<template>
  <div id="app">
    <p>{{ message }}</p>
  </div>
</template>

<script lang="ts">

import { defineComponent } from 'vue'

interface Book {
  title: string
  author: string
  year: number
}

export default defineComponent({
  name: 'App',
  data() {
    return {
      message: 'Hello World!',
      book: {
        title: 'Test',
        author: 'Mayo',
        year: 2021
      } as Book
    }
  }
});
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
	font-weight: bold;
	color: #2c3e50;

	&.router-link-exact-active {
    color: #42b983;
	}
  }
}
</style>

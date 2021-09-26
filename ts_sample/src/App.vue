<template>
  <div id="app">
    <p>{{ message }}</p>
  </div>
</template>

<script lang="ts">

import { defineComponent, PropType } from 'vue'

interface Book {
  title: string
  author: string
  price: number
  onsale?: boolean
}

export default defineComponent({
  name: 'App',
  data() {
    return {
      message: 'Hello World!',
    }
  },
  props: {
    bookA: {
      type: Object as PropType<Book>,
      default: () => ({
        title: 'Sushi'
      }),
      validator: (book: book) => !!book.title
    },
    bookB: {
      type: Object as PropType<Book>,
      default(this: void) {
        return {
          title: 'Kaisendon'
        }
      },
      validator(this: void, book: book) {
        return !! book.title
      }
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

<template>
  <div id="app">
    <p>{{ message }}</p>
    <input type="text" @change="handleChange" />
  </div>
</template>

<script lang="ts">

import { defineComponent } from 'vue'

export default defineComponent({
  name: 'App',
  data() {
    return {
      message: 'Hello World!',
    }
  },
  setup() {
    const handleChange = (evt: Event) => {
      console.log((evt.target as HTMLInputElement).value);
    }

    return { handleChange }
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

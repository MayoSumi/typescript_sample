<template>
  <div id="app">
	<p>{{ name }} - {{ age }}</p>
	<button @click="changeName('Bob')">change name</button>
	<button @click="changeAge(90)">change age</button>
  </div>
</template>

<script lang="ts">

import { defineComponent } from 'vue'

export default defineComponent({
  name: 'App',
  components: {},
  data() {
	return {
    name: 'Link',
    age: 40
	}
  },
  methods: {
	changeName(name: string) {
    this.name = name
	},
	changeAge(age: number) {
    this.age = age
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

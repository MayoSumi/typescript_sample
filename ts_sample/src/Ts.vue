<script lang="ts">

import { defineComponent } from 'vue'

export default defineComponent({
	name: 'App',
	components: {},
	data() {
    return {
		message: 'Hello World!'
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
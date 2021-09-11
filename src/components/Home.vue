<template>
	<h1 class="text-2xl transform rotate-6 mb-2">vue3/vite/vuex/vue-router/tailwindcss template</h1>
	<button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full" @click="increment">
		count is: {{ count }}
	</button>
</template>
<script>
import { mapState, mapActions } from 'vuex';
export default {
	computed: mapState({
		count: (state) => state.counter.count,
	}),
	methods: mapActions({
		increment: 'counter/increment',
	}),
};
</script>

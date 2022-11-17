<template>
	<div>
		<button v-on:click="plus">카운터 : {{ counter }}</button>
	</div>
</template>

<script>
import { ref } from 'vue';
export default {
	setup() {
		const counter = ref(0);
		const plus = () => {
			return counter.value++;
		};

		return { counter, plus };
	},
};
</script>

<style lang="scss" scoped></style>

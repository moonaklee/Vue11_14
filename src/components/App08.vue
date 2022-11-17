<template>
	<div></div>
</template>

<script>
export default {
	setup() {
		const original = reactive({
			count: 0,
		});
		// original -> 작동
		// copy -> 작동
		const copy = readonly(original);
		original.count++;
		copy.count++;
		console.log(original.count);
		console.log(copy.count);
		return {};
	},
};
</script>

<style lang="scss" scoped></style>

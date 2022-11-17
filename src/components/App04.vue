<template>
	<div>
		<!-- v-on:이벤트="메소드이름" -->
		<button v-on:click="plus">click : {{ state.count }}</button>
		<button v-on:click="lpus">click : {{}}</button>
		<!--     <button @click=""></button> -->
	</div>
</template>

<script>
export default {
	// 복합데이터, 원시데이터로
	setup() {
		const state = reactive({
			count: 0,
			main: {
				count: 0,
			},
		});
		const plus = () => {
			return state.count++;
		};
		return { state, plus };
	},
};
</script>

<style lang="scss" scoped></style>

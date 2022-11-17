<template>
	<div></div>
</template>

<script>
import { ref, reactive } from 'vue';
export default {
	setup() {
		const count = ref(0);
		const state = reactive({
			// count : count
			count,
		});
		count.value++;
		console.log(count.value);
		console.log(state.count);
		// ref 원시데이터 -> reactive 복합데이터 안에 객체로 사용하려면 -> value 없이 속성 출력
		// ref 가 reactive 배열로 쓸때는 - value 꼭 포함 속성.value
		//ref -> Array
		const message = ref('hello');
		const arr = reactive([message]);
		console.log(arr[0].value);

		return { count, state };
	},
};
</script>

<style lang="scss" scoped></style>

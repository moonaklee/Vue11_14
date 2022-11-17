<template>
	<div>
		<h2>이름</h2>
		<p>{{ room }}</p>
	</div>
</template>

<script>
import { ref, computed } from 'vue';
export default {
	setup() {
		const first = ref('프론트엔드');
		const sub = ref('전문반');
		const counter = ref(0);
		const room = computed({
			get() {
				return first.value + sub.value;
			},
			set(value) {
				[first.value, sub.value] = value.split(' ');
			},
		});
		console.log('console출력값', room.value);
		room.value = '그래픽 전문가반';

		return { room, counter };
	},
};
</script>

<style lang="scss" scoped></style>

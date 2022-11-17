<template>
	<div>
		<h2>{{ room.name }}</h2>
		<p>{{ hasRoom }}</p>
		<p>{{ actionRoom() }}</p>
	</div>
</template>

<script>
export default {
	setup() {
		const room = reactive({
			name: '프론트엔드',
			etc: ['html', 'css', 'javascript'],
		});
		const hasRoom = computed(() => {
			console.log('computed');
			return room.etc.length > 0 ? '과목이 있다.' : '과목이 없다.';
		});
		const actionRoom = () => {
			console.log('methods');
			return room.etc.length > 0 ? '있음' : '없음';
		};
		return { room, hasRoom, actionRoom };
	},
};
</script>

<style lang="scss" scoped></style>

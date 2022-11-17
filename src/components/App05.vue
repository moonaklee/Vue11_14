<template>
	<div>
		<p>{{ i }}</p>
		<p>{{ str }}</p>
	</div>
</template>

<script>
import { ref } from 'vue';
export default {
	setup() {
		let i = ref(1);
/* 		let str = 'str'; */
    const addStr = () => {
/*       str = str + '!';
    } */

		return { i, str };
	},
};
}
</script>

<style lang="scss" scoped></style>

<!-- 옵션방법 vbase -->
<template>
	<div>
		<button v-on:click="plus">카운트 : {{ counter }}</button>
	</div>
</template>
<script>
import {onMounted} from 'vue';


export default {
	data() {
		return { counter: 0 };
	},
	methods: {
    plus(){
      this.counter++;
    };
	},
	mounted() {
/* 		console.log('mount end'); */
	},
};
</script>

<style scoped></style>

<template>
	<div>
		<p>author : {{ author }}</p>
		<p>title : {{ title }}</p>
	</div>
</template>

<script>
import { reactive } from 'vue';
export default {
	setup() {
		const book = reactive({
			author: 'Vue Team',
			year: 2022,
			title: 'Vue3',
		});
		/* 		const { author, title } = book; */
		// const {author,title} = toRefs(book)
		const author = toRef(book, 'author');
		const title = toRef(book, 'title');
		return { author, title, book };
	},
};
</script>

<style lang="scss" scoped></style>

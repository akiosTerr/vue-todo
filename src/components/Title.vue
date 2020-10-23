<template>
	<div class="title-container">
		<h2>hello</h2>
		<h3>{{ msg }}</h3>
	</div>
</template>
<script>
export default {
	name: 'Title',
	props: {
		msg: Number,
	},
};
</script>

<style></style>

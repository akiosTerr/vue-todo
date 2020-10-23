<template>
	<div class="todo-item">
		<input type="checkbox" name="isdone" id="is-done" />
		<h3>{{ todo.title }}</h3>
	</div>
</template>

<script>
export default {
	name: 'TodoItem',
	props: ['todo'],
};
</script>

<style scoped>
.todo-item {
	display: flex;
	flex-direction: row;
	color: rgb(1, 248, 42);
	background: #555;
	width: 200px;
	justify-content: baseline;
	align-items: center;
	margin-bottom: 10px;
}

.is-complete {
	text-decoration: line-through;
}
</style>

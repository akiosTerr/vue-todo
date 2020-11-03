<template>
	<div class="todos">
		<TodoItem
			v-bind:todo="todo"
			v-on:del-todo="$emit('del-todo', todo.id)"
			v-bind:key="todo.id"
			v-for="todo in todos"
		/>
	</div>
</template>

<script>
import TodoItem from './TodoItem';

export default {
	name: 'Todos',
	components: {
		TodoItem,
	},
	props: ['todos'],
};
</script>

<style scoped>
.todos {
	display: flex;
	flex-direction: column;
	align-items: center;
	width: 400px;
	margin: auto;
}
</style>

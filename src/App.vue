<template>
	<div id="app">
		<HelloWorld msg="TODO APP" />
		<Todos v-bind:todos="todos" v-on:del-todo="deleteItem" />
	</div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import Todos from './components/Todos.vue';

export default {
	name: 'App',
	components: {
		HelloWorld,
		Todos,
	},
	methods: {
		deleteItem(id) {
			console.log(id);
			this.todos = this.todos.filter((todo) => todo.id != id);
		},
	},
	data() {
		return {
			todos: [
				{ id: 1, title: 'dishes', completed: false },
				{ id: 2, title: 'work task', completed: false },
				{ id: 3, title: 'put the trashout', completed: false },
			],
		};
	},
};
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
</style>

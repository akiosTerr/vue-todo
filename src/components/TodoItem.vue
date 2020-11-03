<template>
	<div class="todo-item" v-bind:class="{ 'is-complete': todo.completed }">
		<div class="item-head">
			<input class="toggle-box" type="checkbox" v-on:change="markComplete" />
			<p>{{ todo.title }}</p>
		</div>
		<button @click="$emit('del-todo', todo.id)" class="del">X</button>
	</div>
</template>

<script>
export default {
	name: 'TodoItem',
	props: ['todo'],
	methods: {
		markComplete() {
			this.todo.completed = !this.todo.completed;
		},
	},
};
</script>

<style scoped>
.todo-item {
	display: flex;
	flex-direction: row;
	color: #f8be01;
	background: rgb(102, 56, 56);
	width: 100%;
	justify-content: space-between;
	align-items: center;
	margin-bottom: 10px;
}

.toogle-box {
	padding: 20px;
}

.item-head {
	display: flex;
	flex-direction: row;
	align-items: center;
}

.is-complete {
	text-decoration: line-through;
}

.del {
	color: black;
	background: red;
}
</style>

<template>
	<div id="app">
		<Header v-on:createTodo="createTodo" />
		<Todos v-bind:todos="todos" v-on:removeTodo="removeTodo" />
	</div>
</template>

<script>
	import Header from './components/Header';
	import Todos from './components/Todos';
	let todos = [
		{
			id: "1",
			name: "Record Video",
			done: false
		},
		{
			id: "2",
			name: "Upload Video",
			done: false
		},
		{
			id: "3",
			name: "partayy",
			done: false
		},
		{
			id: "4",
			name: "Debug",
			done: false
		},
		{
			id: "5",
			name: "More Debug",
			done: false
		}
	];
	export default {
		name: 'app',
		components: {
			Header,
			Todos
		},
		data: function () {
			return {
				todos: todos
			}
    },
  }
</script>

<style lang="scss">
body {
  margin: 0;
  padding: 0;
  background: #2E4272;
  font-family: Arial, Helvetica, sans-serif;
}
</style>

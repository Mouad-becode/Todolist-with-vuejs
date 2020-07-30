<template>
    <section id="todos">
        <div class="todo" v-for="(todo) in todos" :key="todo.id">
           <label>
           <input type="checkbox" name="done" v-if="todo.done" checked> 
           <input type="checkbox" name="done" v-else> 
           {{ todo.name }}
           <button class="Remove" v-on:click="() => removeTodo(todo.id)">Remove</button>
           </label>
           
        </div> 
    </section>
</template>

<script>
    export default {
        name:"Todos",
        props:["todos"],
            methods: {
                removeTodo: function (id) {
                    this.$emit("removeTodo", id)
                }
            }
    }
</script>

<style lang="scss" scoped>
    #todos {
        display: flex;
		flex-direction: row;
		justify-content: center;
		flex-wrap: wrap;
		width: 100%;

        .todo {
			display: flex;
            width: 24%;

             
             
			
            label {
				flex: 1;
                user-select: none;
                margin: 15px;
                padding: 15px;
                background: #FFF;
                display: flex;
                justify-content: space-between;
                align-items: center;
    
                
			}

		}
    }
</style>
<template>
    <section id="todos">
        <div class="todo" v-for="(todo) in todos" :key="todo.id">
           <label>
           <input type="checkbox"> {{ todo.name }}
           </label>
        </div> 
    </section>
</template>

<script>
    export default {
        name:"Todos",
        props:["todos"],
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
                
			}
		}
    }
</style>
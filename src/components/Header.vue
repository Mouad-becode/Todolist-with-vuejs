
<template>
	<header>
		<input type="text" name="todoInput" v-model="todoValue" placeholder="What you want to do?" />
		<button class="submit" id="createTodo" >+</button>
	</header>
</template>



<script>
export default {
    name:"Header"
}
</script>

<style lang="scss" scoped>
    header{
        display: flex;
        text-align: center;
        input {
            flex: 1;
            height: 50px;
            box-sizing: border-box;
            font-size: 20px;
            text-indent: 15px;
        
        }

        .submit {
width: 50px;
			height: 50px;
			color: #171717;
			font-size: 28px;
			line-height: 1;
			font-weight: 700;
			background-color: white;
			border: none;
			outline: none;
            border-radius: 50%;
			cursor: pointer;

			&:hover {
				background-color: lighten($color: green, $amount: 10);
			}
			&:active {
background-color: lighten($color: green, $amount: 5);			}
        }


    }

</style>
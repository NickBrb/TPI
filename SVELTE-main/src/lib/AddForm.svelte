<script>
    import {todos} from "./store"

    let nuovoTodo

    function AddTodo() {
        todos.update((old) =>{
            old.push({
                title : nuovoTodo, 
                done : false 
            }) 
            return old
        })
    }

</script>

<input type ="text" bind:value={nuovoTodo} class="input input-bordered w-full max-w-xs"/>
<br>
<button on:click={AddTodo}  class="text-white bg-blue-700 hover:bg-blue-800 focus:outline-none focus:ring-4 focus:ring-blue-300 font-medium rounded-full text-sm px-5 py-2.5 text-center me-2 mb-2 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800 mt-4">Add </button>


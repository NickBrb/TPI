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
<br><br>
<button on:click={AddTodo}  class="bg-white hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded shadow"> Add... </button>


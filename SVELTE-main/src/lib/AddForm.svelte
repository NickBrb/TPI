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
<button on:click={AddTodo} class="btn btn-outline btn-info"> Aggiungi </button>


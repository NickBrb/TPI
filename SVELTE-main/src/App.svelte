<script>
   import ListaTodo from "./lib/ListaTodo.svelte"
   import TodoCounter from "./lib/TodoCounter.svelte"  
   
   import {todos} from "./lib/store"
   import AddForm from "./lib/AddForm.svelte"

</script>

<main>
  <h1>to do list </h1>  
  <TodoCounter />
  <AddForm />
  <ListaTodo todoList ={$todos} />

  
</main>

<style>
 
</style>

<script>
   import ListaTodo from "./lib/ListaTodo.svelte"
   import TodoCounter from "./lib/TodoCounter.svelte"  
   
   import {todos} from "./lib/store"
   import AddForm from "./lib/AddForm.svelte"

</script>

<main>
  <h1 class="mb-4 text-4xl font-extrabold leading-none tracking-tight text-gray-900 md:text-5xl lg:text-blue-900 dark:text-blue-600">TO DO LIST </h1>  
  <TodoCounter />
  <AddForm />
  <ListaTodo todoList ={$todos} />

  
</main>

<style>
 
</style>

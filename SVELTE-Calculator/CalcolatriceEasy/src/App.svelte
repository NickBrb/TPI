<script>
  import svelteLogo from './assets/svelte.svg'
  import viteLogo from '/vite.svg'
  import Counter from './lib/Counter.svelte'

  let total =0;
  let console ="";
  let state = null;

  function resolveState(){

  }

  function setOperation(operation){

  }

  function setValue(value){

  }

  function equal(){

  }
</script>


<style>
.calculator{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 300px;
  border: 1px solid #eee;
  box-shadow: 2px 2px 2px #eee;
  padding:10px;
}
</style>
<div class="calculator">
  <input type="text" bind:value={console}/>
  <div class="buttons">
    
      
      <button on:click={()=>{setOperation('add')}}>
        +
      </button>

      <button on:click={()=>{setOperation('substract')}}>
        -
      </button>

      <button on:click={()=>{setOperation('multiply')}}>
        &times;
      </button>

      <button on:click={()=>{setOperation('divide')}}>
        &divide;
      </button>
  </div>
  <div class="operations">

  </div>
  <div class="numbers">
    <div>
      <button on:click={()=>{setValue(7);}}>
        7
      </button>
      <button on:click={()=>{setValue(8);}}>
        8
      </button>
      <button on:click={()=>{setValue(9);}}>
        9
      </button>
    </div>
    <div>
      <button on:click={()=>{setValue(4);}}>
        4
      </button>
      <button on:click={()=>{setValue(5);}}>
        5
      </button>
      <button on:click={()=>{setValue(6);}}>
        6
      </button>
    </div>
    <div>
      <button on:click={()=>{setValue(1);}}>
        1
      </button>
      <button on:click={()=>{setValue(2);}}>
        2
      </button>
      <button on:click={()=>{setValue(3);}}>
        3
      </button>
    </div>
    <div>
      <button on:click={()=>{setValue(0);}}>
        0
      </button>
      <button on:click={()=>{setValue('.');}}>
        .
      </button>
      <button on:click={()=>{setValue('C');}}>
        C
      </button>
    </div>
    <div class="equal">
      <button on:click={equal}>
        =
      </button>
    </div>
    
  </div>
</div>

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
    resolveState();
    state = operation;
  }

  function setValue(value){
    if(console.toString() == "0" || state == "equal"){
      console = "";
    }
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
.calculator .input{
    width: 100%;
    padding: 20px;
    outline: none;
    text-align: right;
    font-size: 20px;    
}
.calculator .buttons{
  display: flex;
  flex-wrap: wrap;
}
.calculator .buttons .operations{
    display: flex;
    justify-content: space-between;
    width: 100%;
}
.calculator .buttons.operations button{
  width: 24%;
}
.calculator .buttons .numbers{
  width: 75%;
}
.calculator .buttons .numbers > div{
  display: flex;
  justify-content: space-between;
}
.calculator.buttons.numbers > div button{
  width: 32%; 
}
.calculator .equal{
  flex: 1; 
}
.calculator .equal button{
  margin-left: 5%;
  width: 95%;
  height: 95%;
  background: #00acee;
  color: #eee;
}

.calculator button {
  outline: none;
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

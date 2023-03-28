<script>
     let listItem = '';
     let listList = [];

     function add(){
          if (listItem == '') {
               return;
          }
          listList = [...listList, {
               text: listItem,
               done: false
          }]
          listItem = '';
     }

     function removeList(index) {
          listList.splice(index, 1);
          listList = listList;
     }

     function clearDone(){
          listList = listList.filter(t => !t.done);
     }

     function clearAll(){
          listList = [];
     }

</script>


<form on:submit|preventDefault={add}>

     <input bind:value={listItem} type="text" autofocus/><button type="submit">Add</button>

</form>


<ul>
     {#each listList as item, index}
          <li>
               <input type="checkbox" bind:checked={item.done}>
               <span class:done={item.done}>{item.text}</span>
               <span on:click={() => removeList(index)} on:keypress={() => removeList(index)} class="remove"></span>
          </li>
     {/each}
</ul>

<button on:click={clearDone} class="clearDone">Clear Completed</button>

<button on:click={clearAll}>Clear All</button>


<style>
     button {
          font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
          font-size: 1em;
          border-radius: 0.25em;
          background-color: rgb(0, 145, 255);
          color: aliceblue;
          padding: 0.75vh;
          border: none;

     }

     .clearDone {
          color: rgb(0, 145, 255);
          background-color: aliceblue;

     }

     ul {
          list-style: none;
          font-family: Verdana, Geneva, Tahoma, sans-serif;
     }

     .done{
          text-decoration: line-through;
          color: rgb(164, 0, 0);
     }

     .remove {
          height: 1rem;
          width: 1rem;
          display: inline-block;
          background: url('./images/trash-can.png')
          no-repeat;
          background-size: 100% auto;
          cursor: pointer;
     }

</style>
<script>
     import ListApp from './ListApp.svelte';
</script>

<header><h1>To Do List App</h1></header>


<ListApp />

<style>
     :global(body) {
          background-color: rgb(53, 53, 53);
          color: rgb(233, 233, 233);
          font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
          margin: 0;
     }

     :global(header) {
          background-color: rgb(164, 0, 0);
          
          
     }

     h1 {
          margin: 0;
     }
</style>
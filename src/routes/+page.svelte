<script>
     import ListApp from './ListApp.svelte';
</script>

<header><h1>To Do List App</h1></header>


<ListApp />

<style>
     :global(body) {
          background-color: rgb(233, 233, 233);
          color: rgb(53, 53, 53);
          font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
     }

     :global(header) {
          background-color: rgb(164, 0, 0);;
     }
</style>
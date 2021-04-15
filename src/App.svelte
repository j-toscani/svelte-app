<!-- App.svelte -->
<script lang="typescript">
  import Nested from "./Nested.svelte";
</script>

<div class="App">
  <header class="App-header" />

  <main>
    <Nested answer={"42"} />
  </main>
</div>

<style>
  /* css will go here */
</style>

<!-- App.svelte -->
<script lang="typescript">
  import Nested from "./Nested.svelte";

  let count = 0;

  function handleClick() {
    count += 1;
  }

  $: doubled = count * 2;
</script>

<div class="App">
  <header class="App-header">
    <a
      class="App-link"
      href="https://svelte.dev"
      target="_blank"
      rel="noopener noreferrer"
    >
      Learn Svelte
    </a>
  </header>

  <main>
    <button on:click={handleClick}> Add </button>
    <span>
      Counter is : {count}
    </span>
    <span>
      Doubled {doubled}
    </span>

    <Nested answer={"42"} />
  </main>
</div>

<style>
  /* css will go here */
</style>

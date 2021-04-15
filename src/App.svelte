<!-- App.svelte -->
<script lang="typescript">
  let count = 0;

  function handleClick() {
    count += 1;
  }

  // Computed Prop
  $: doubled = count * 2;

  function logCount(count: number) {
    console.log(`The count is ${count}`);
  }

  // Computed Prop
  $: logCount(count);
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
    <span> Counter is : {count}</span>
    <span>Doubled: {doubled} </span>
  </main>
</div>

<style>
  /* css will go here */
</style>

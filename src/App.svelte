<!-- App.svelte -->
<script lang="typescript">
  import Nested from "./Nested.svelte";
  import Info from "./Info.svelte";
  import LoginButtons from "./LoginButtons.svelte";

  let count = 0;

  function handleClick() {
    count += 1;
  }

  $: doubled = count * 2;

  const pkg = {
    name: "svelte",
    version: 3,
    speed: "blazing",
    website: "https://svelte.dev",
  };
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
    <Info {...pkg} />
    <LoginButtons />
  </main>
</div>

<style>
  /* css will go here */
</style>

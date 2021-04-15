<script>
  let user = { loggedIn: false };

  function toggle() {
    user.loggedIn = !user.loggedIn;
  }
</script>

<button on:click={toggle}>
  {#if user.loggedIn}
    Log Out
  {:else}
    Log In
  {/if}
</button>

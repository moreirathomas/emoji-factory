<script>
  export let placeholder;
  export let input;
  export let func;
  const clear = () => (input = "");
</script>

<style>
  input {
    max-width: 180px;
    background: var(--light-background);
    color: var(--light-color);
    border: 2px solid var(--dark-background);
  }
  :global(body.dark-mode) input {
    background: var(--dark-background);
    color: var(--dark-color);
    border: 2px solid var(--light-background);
  }
  input:focus {
    border: 3px solid var(--action-color) !important;
  }
  button {
    background-color: var(--accent-color);
    color: var(--dark-color);
  }
  button:active {
    background-color: var(--action-color);
  }
</style>

<div class="input-wrapper">
  <input type="text" {placeholder} bind:value={input} on:input={func} />

  <button on:click={clear}>
    <i class="fas fa-times-circle" />
  </button>
</div>

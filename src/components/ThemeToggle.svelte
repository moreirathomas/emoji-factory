<script>
  let darkMode = false;
  const toggleMode = () => {
    window.document.body.classList.toggle("dark-mode");
    darkMode = !darkMode;
  };
</script>

<style>
  button {
    background-color: var(--dark-background);
    color: var(--dark-color);
    margin: 0;
  }
  :global(body.dark-mode) button {
    background-color: var(--light-background);
    color: var(--light-color);
  }
</style>

<button on:click={toggleMode}>
  <i class="fas {darkMode ? 'fa-sun' : 'fa-moon'}" />
</button>

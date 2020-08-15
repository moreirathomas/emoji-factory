<script>
  export let result;
  export let placeholder;
</script>

<style>
  div.result-chip {
    display: inline-flex;
    align-items: center;
    max-width: 240px;
    height: 2rem;
    border-radius: 16px;
    padding: 0 1rem;
    background: var(--dark-background);
    color: var(--dark-color);
  }
  :global(body.dark-mode) div.result-chip {
    background: var(--light-background);
    color: var(--light-color);
  }
  span.result {
    margin: 0 1rem;
  }
</style>

<div class="result-chip">
  <i class="fas fa-arrow-circle-right" />
  <span class="result">{result || placeholder}</span>
</div>

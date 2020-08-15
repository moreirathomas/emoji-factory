<script>
  export let string;
</script>

<style>
  div.result-chip {
    display: inline-flex;
    align-items: center;
    height: 2rem;
    border-radius: 16px;
    padding: 0 1rem;
    background: #333;
    /* max-width: max-content; */
  }
  span.result {
    margin: 0 1rem;
  }
</style>

<div class="result-chip">
  <i class="fas fa-arrow-circle-right" style="color: #fff" />
  <span class="result">{string}</span>
</div>

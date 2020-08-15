<script>
  import { onMount } from "svelte";
  import ResultChip from "./ResultChip.svelte";

  let input = "🏳🌈";
  let result;

  const combine = emojis => {
    return emojis.reduce((a, b) => a + "\u200d" + b);
  };
  const combineHandler = emojis => {
    emojis.length ? (result = combine([...emojis.trim()])) : (result = "");
  };

  onMount(() => combineHandler(input));
</script>

<style>

</style>

<div class="container">
  <input
    type="text"
    placeholder="Combine emojis"
    bind:value={input}
    on:input={combineHandler(input)} />

  <ResultChip string={result} />
</div>

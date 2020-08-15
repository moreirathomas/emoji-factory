<script>
  import { onMount } from "svelte";
  import ResultChip from "./ResultChip.svelte";

  let input = "👨‍👩‍👦‍👦";
  let result;

  const spread = emoji => {
    return [...emoji].filter(el => el !== "\u200d");
  };
  const spreadHandler = emoji => {
    result = spread(emoji.trim());
  };

  onMount(() => spreadHandler(input));
</script>

<style>

</style>

<div class="container">
  <input
    type="text"
    placeholder="Spread an emoji"
    bind:value={input}
    on:input={spreadHandler(input)} />

  <ResultChip string={result} />
</div>

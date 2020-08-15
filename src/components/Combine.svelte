<script>
  import { onMount } from "svelte";
  import InputChip from "./InputChip.svelte";
  import ResultChip from "./ResultChip.svelte";

  let input = "🏳🌈";
  let result;
  let placeholder = "Combine them!";

  const combine = emojis => {
    return emojis.reduce((a, b) => a + "\u200d" + b);
  };
  const combineHandler = emojis => {
    emojis.length ? (result = combine([...emojis.trim()])) : (result = "");
  };

  onMount(() => combineHandler(input));
</script>

<div class="container">
  <InputChip
    placeholder={'Some nice emojis'}
    bind:input
    func={combineHandler(input)} />
  <ResultChip {result} {placeholder} />
</div>

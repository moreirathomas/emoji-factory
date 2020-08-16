<script>
  import { onMount } from "svelte";
  import InputChip from "../view/InputChip.svelte";
  import ResultChip from "../view/ResultChip.svelte";

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

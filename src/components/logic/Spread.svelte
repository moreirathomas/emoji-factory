<script>
  import { onMount } from "svelte";
  import InputChip from "../view/InputChip.svelte";
  import ResultChip from "../view/ResultChip.svelte";

  let input = "👨‍👩‍👦‍👦";
  let result;
  let placeholder = "Spread it!";

  const spread = emoji => {
    return [...emoji].filter(el => el !== "\u200d" && el !== "");
  };
  const spreadHandler = emoji => {
    emoji.length ? (result = spread(emoji.trim())) : (result = "");
  };

  onMount(() => spreadHandler(input));
</script>

<div class="container">
  <InputChip
    placeholder={'One good emoji'}
    bind:input
    func={spreadHandler(input)} />
  <ResultChip {result} {placeholder} />
</div>

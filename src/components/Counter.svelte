<script>
  import { onMount } from "svelte";
  let count = 0;

  function add() {
    count += 1;
  }

  function subtract() {
    count -= 1;
  }
  onMount(() => console.log("onMount"));
</script>

<div class="counter">
  <button on:click={subtract}>-</button>
  <pre>{ count }</pre>
  <button on:click={add}>+</button>
</div>
<div class="children">
  <slot />
</div>

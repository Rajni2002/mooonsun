<script lang="ts">
  let { children, ...others } = $props();
  // everything else (data-*, aria-*, class, etc.) can be passed through $$restProps
</script>

<button
  data-tally-open="LZZG1J"
  data-tally-layout="modal"
  data-tally-width="700"
  data-tally-emoji-text="👋"
  data-tally-emoji-animation="wave"
  data-tally-form-events-forwarding="1"
  {...others}
>
  {@render children()}
</button>

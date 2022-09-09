<script>
  import { createEventDispatcher } from "svelte";

  export let id = window.crypto.randomUUID();
  export let open = false;
  export let bgColor = "";
  export let border = "";

  const dispatch = createEventDispatcher();
</script>

<input type="checkbox" {id} bind:checked={open} class="modal-toggle" />
<div class="modal">
  <div class="modal-box {bgColor} {border}">
    <slot />
  </div>
</div>

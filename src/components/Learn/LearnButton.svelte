<script>
  import Button from "sveltestrap/src/Button.svelte";

  import { faBook } from "@fortawesome/free-solid-svg-icons/faBook";
  import Fa from "svelte-fa";
  let icon = faBook;

  export let text;
</script>

<Button color="warning">
  <Fa {icon} size="sm" />
  {text}
</Button>

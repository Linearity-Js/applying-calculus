<script>
  import { Router } from "@sveltech/routify";
  import { routes } from "@sveltech/routify/tmp/routes";
  import Main from "../components/Main.svelte";
</script>

<Main>
  <Router {routes} />
</Main>

<script>
  import Logo from "../components/Logo.svelte";

  import { faBook } from "@fortawesome/free-solid-svg-icons/faBook";
  import Fa from "svelte-fa";
  let icon = faBook;

  import { isDark } from "../stores/stores";
  import Button from "sveltestrap/src/Button.svelte";
  import Login from "../components/Login.svelte";

  import { url } from "@sveltech/routify";

  isDark.subscribe((value) => {
    value
      ? document.body.classList.add("dark")
      : document.body.classList.remove("dark");
  });

  function handleDarkMode() {
    $isDark = !$isDark;
  }

  export let open;
  open = false;
  const toggle = () => (open = !open);
</script>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@800&display=swap");
  :global(:root) {
    --light-theme-body-background: #ffff;
    --dark-theme-body-background: #1c1e21;
  }

  :global(body) {
    background-color: var(--light-theme-body-background);
    transition: 0.3s ease;
  }

  :global(body.dark) {
    background-color: var(--dark-theme-body-background);
    color: white;
  }

  :global(Button) {
    font-family: "Montserrat", sans-serif;
    /* text-transform: uppercase; */
    padding: 0.5rem 2.5rem !important;
    margin-top: 1rem;
    margin-bottom: 1rem;
    line-height: 1.5 !important;
    color: white !important;
    font-size: 2rem !important;
    border-radius: 1rem !important;
    outline: none !important;
    border: none !important;
  }
  :global(Button):focus {
    box-shadow: none !important;
  }
</style>

<div class="Index">
  <Login {open} on:click={toggle} />
  <Logo />
  <a href={$url('../learn')}>
    <Button color="warning">
      <Fa {icon} size="sm" />
      Learn
    </Button>
  </a>
  <!-- button on:click={handleDarkMode}>dark mode</button> -->
</div>

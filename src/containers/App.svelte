<script>
  import Header from "../components/Header.svelte";
  import Logo from "../components/Logo.svelte";
  import Button from "../components/Button.svelte";
  import Main from "../components/Main.svelte";

  import { isDark } from "../stores/stores";

  isDark.subscribe((value) => {
    value
      ? document.body.classList.add("dark")
      : document.body.classList.remove("dark");
  });

  function handleDarkMode() {
    $isDark = !$isDark;
  }
</script>

<style>
  :global(:root) {
    --light-theme-body-background: #ebedf0;
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
</style>

<Header />
<Main>
  <Logo />
  <Button />
</Main>

<button on:click={handleDarkMode}>dark mode</button>

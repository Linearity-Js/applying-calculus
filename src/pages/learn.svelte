<script>
  import Logo from "../components/Logo.svelte";
  import UserHeader from "../components/Header/UserHeader.svelte";
  import LearnButton from "../components/Learn/LearnButton.svelte";

  import { url } from "@sveltech/routify";

  const buttons = [
    ["/index", "Errores"],
    ["/index", "Optimizacion"],
    ["/index", "Graficación"],
    ["/index", "Area bajo la curva"],
    ["/index", "Solidos de Revolución"],
    ["/index", "Series"],
  ];
</script>

<style>
  a {
    margin-left: 1rem;
    margin-right: 1rem;
  }
</style>

<UserHeader />
<Logo />
{#each buttons as [path, text]}
  <a href={$url(path)}>
    <LearnButton {text} />
  </a>
{/each}

<script>
  // import Button from "sveltestrap/src/Button.svelte";
  import Icon from "fa-svelte";
  import { faMoon } from "@fortawesome/free-solid-svg-icons/faMoon";
  import { isDark } from "../stores/stores";
  const changeMode = () => ($isDark = !$isDark);
  let icon = faMoon;
</script>

<style>
  .profile__switch {
    background: linear-gradient(to right, #4ee8f3, #270e47) !important;
    border-radius: 100px;
    border: none;
    position: relative;
    cursor: pointer;
    outline: none;
    padding: 0;
    display: flex;
    /* font-size: 1.9em; */
  }

  .profile__switch:after {
    content: "";
    width: 30px;
    height: 30px;
    border-radius: 100px;
    background-color: var(--white-color);
    position: absolute;
    left: 0;
    box-shadow: 0px 0px 2px 2px rgba(0, 0, 0, 0.2);
    transition: transform linear 0.3s;
  }
  .profile__switch.active:after {
    transform: translateX(30px);
  }

  .profile__icon {
    width: 30px;
    height: 30px;
    line-height: 30px;
    color: var(--white-color);
  }
</style>

<div>

  <button class="profile__switch" class:active={$isDark} on:click={changeMode}>
    <span class="profile__icon">
      <Icon {icon} />
    </span>
    <span class="profile__icon">
      <Icon {icon} />
    </span>
  </button>

  <!-- {#if $isDark}
    <Button color="light" on:click>
      <span>
        Theme
        <Icon {icon} />
      </span>
    </Button>
  {:else}
    <Button color="dark" on:click>
      <span>
        Theme
        <Icon {icon} />
      </span>
    </Button>
    <Button color="dark" on:click>darkMode</Button>
  {/if} -->
</div>

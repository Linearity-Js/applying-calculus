<script>
  import Header from "./Header.svelte";
  import { NavItem, NavLink } from "sveltestrap";

  import { faGithub } from "@fortawesome/free-brands-svg-icons";
  import Fa from "svelte-fa";
  let icon_git = faGithub;
</script>

<Header>
  <NavItem>
    <NavLink
      href="https://github.com/RubioHaro/applying-calculus"
      target="__blank">
      <Fa icon={icon_git} size="3x" primaryColor="gold" />
    </NavLink>
  </NavItem>
</Header>

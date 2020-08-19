<script>
  import Header from "./Header.svelte";
  import { NavItem, NavLink } from "sveltestrap";
  
  import Fa from "svelte-fa";
  import { faUser } from "@fortawesome/free-solid-svg-icons/faUser";
  let icon_usr = faUser;
</script>

<Header>
  <NavItem>
    <NavLink>
      <Fa icon={icon_usr} size="3x" primaryColor="gold" />
    </NavLink>
  </NavItem>
</Header>

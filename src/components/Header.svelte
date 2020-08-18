<script>
  import { faGithub } from "@fortawesome/free-brands-svg-icons";
  import { Navbar, Nav, NavItem, NavLink } from "sveltestrap";
  import Fa from "svelte-fa";
  let icon = faGithub;
</script>

<Navbar light expand="md">
  <Nav class="ml-auto" navbar>
    <NavItem>
      <NavLink href="https://github.com/RubioHaro/applying-calculus" target="__blank">
        <Fa {icon} size="5x" primaryColor="gold"/>
      </NavLink>
    </NavItem>
  </Nav>
</Navbar>

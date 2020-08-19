<script>
  import { Navbar, Nav } from "sveltestrap";
</script>

<Navbar light expand="md">
  <Nav class="ml-auto" navbar>
    <slot />
  </Nav>
</Navbar>

<script>
  import App from "../containers/App.svelte";
  import img from "../img/logo.png";
  import { Col, Container, Row } from "sveltestrap";
  import { fade } from "svelte/transition";
  let visible = false;
  import { onMount } from "svelte";
  onMount(async () => {
    if (!visible) {
      setTimeout(1000);
      visible = true;
    }
  });
</script>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@800&display=swap");
  .Logo-title {
    font-family: "Montserrat", sans-serif;
    text-transform: uppercase;
    font-size: 5rem;
  }

  .flex-center-vertically {
    display: flex;
    justify-content: center;
    flex-direction: column;
    height: 400px;
  }
</style>

{#if visible}
  <div class="Logo" transition:fade>

    <Container>
      <Row>
        <Col>
          <div class="Logo-image">
            <img src={img} alt="por definir" />
          </div>
        </Col>
        <Col>
          <div class="Logo-title flex-center-vertically">
            Applying
            <br />
            Calculus
          </div>
        </Col>
      </Row>
    </Container>
  </div>
{/if}

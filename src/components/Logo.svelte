<script>
  import App from "../containers/App.svelte";
  import img from "../img/applying-calculus.png";
  import { Col, Container, Row } from "sveltestrap";
  let visible = true;
</script>

{#if visible}
  <div class="Logo">
    <Container>
      <Row>
        <Col>
          <div class="Logo-image">
            <img class="img-fluid" src={img} alt="por definir" />
          </div>
        </Col>
      </Row>
    </Container>
  </div>
{/if}

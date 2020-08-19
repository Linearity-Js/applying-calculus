<script>
  import {
    Button,
    Modal,
    ModalBody,
    ModalFooter,
    ModalHeader,
  } from "sveltestrap";
  export let open = false;
  import { url } from "@sveltech/routify";
</script>

<style>
  .Login-modal-head {
    font-family: "Montserrat", sans-serif;
    font-size: 2rem !important;
  }
</style>

<div class="Login">

  <Modal isOpen={open} on:click>
    <ModalHeader toggle="on:click">
      <div class="Login-modal-head">Access</div>
    </ModalHeader>
    <ModalBody>
      <Button color="secondary" on:click>
        <a href={$url('../learn')}>Google</a>
      </Button>
      <Button color="secondary" on:click>Github</Button>
    </ModalBody>
    <ModalFooter />
  </Modal>
</div>

<script>
  import { Link } from "svelte-routing";
  import { Form, Input, Label, Container, Row, Col, Button } from "sveltestrap";

  let message;
  let status;
</script>

<section class="bg-login d-flex align-items-center">
  <Container>
    <Row class="justify-content-center mt-4">
      <Col lg={4}>
        <div class="bg-white p-4 rounded">
          <div class="text-center">
            <h4 class="fw-bold mb-3">Payment Failed.</h4>
          </div>
        </div>
        <div class="text-center">
          <h2 class=" mb-3">{message}</h2>
        </div>
        <div class="text-center">
          <p class=" mb-3">{status}</p>
        </div>
        <div class="text-center mt-3">
          <p>
            <small class="me-2">Want to make another payment ?</small>
            <Link to="" class="fw-bold">Pay Again</Link>
          </p>
        </div>
      </Col>
    </Row>
  </Container>
</section>

<script>
  import { Link } from "svelte-routing";
  import { Form, Input, Label, Container, Row, Col, Button } from "sveltestrap";

  // onMount(async () => {
  //   await new Promise((resolve) => setTimeout(resolve, 50000)).then(() => {
  //     navigate("/", { replace: true });
  //   });
  // });
</script>

<section class="bg-login d-flex align-items-center">
  <Container>
    <Row class="justify-content-center mt-4">
      <Col lg={4}>
        <div class="bg-white p-4 rounded">
          <div class="text-center">
            <h4 class="fw-bold mb-3">Payment Succesful.</h4>
          </div>
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

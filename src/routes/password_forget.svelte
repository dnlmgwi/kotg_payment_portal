<script>
  import { Input, Container, Row, Button, Form, Col } from "sveltestrap";
  import { Link } from "svelte-routing";
</script>

<section class="bg-login d-flex align-items-center">
  <Container>
    <Row class="justify-content-center mt-4">
      <Col lg={4} class="col-lg-4">
        <div class="bg-white p-4 mt-5 rounded">
          <div class="text-center">
            <h4 class="fw-bold mb-3">Globing</h4>
          </div>
          <h6 class="text-center text-muted font-weight-normal forgot-pass-txt">
            Enter your email address and we'll send you an email with
            instructions to reset your password.
          </h6>
          <Form class="login-form">
            <Row>
              <Col lg={12} class="mt-3">
                <Input
                  type="email"
                  class="form-control"
                  placeholder="Email"
                  required=""
                />
              </Col>
              <Col lg={12} class="mt-4 mb-2">
                <Button color="primary" class="w-100"
                  >Reset your Password</Button
                >
              </Col>
            </Row>
          </Form>
        </div>
        <div class="text-center mt-3">
          <p>
            <small class="text-white me-2">Already have account?</small>
            <Link to="login" class="text-white fw-bold">Sign in</Link>
          </p>
        </div>
      </Col>
    </Row>
  </Container>
</section>

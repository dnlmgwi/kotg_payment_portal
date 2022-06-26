<script>
  import { Link } from "svelte-routing";
  import { Form, Input, Label, Container, Row, Col, Button } from "sveltestrap";
</script>

<section class="bg-login d-flex align-items-center">
  <Container>
    <Row class="justify-content-center mt-4">
      <Col lg={4}>
        <div class="bg-white p-4 rounded">
          <div class="text-center">
            <h4 class="fw-bold mb-3">Globing</h4>
          </div>
          <Form class="login-form">
            <Row>
              <Col lg={12} class="mt-2">
                <Input
                  type="email"
                  class="form-control"
                  placeholder="Email"
                  required=""
                />
              </Col>
              <Col lg={12} class="mt-2">
                <Input
                  type="password"
                  class="form-control"
                  placeholder="Password"
                  required=""
                />
              </Col>
              <Col lg={12} class="mt-2">
                <div class="form-check">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    value=""
                    id="flexCheckDefault"
                  />
                  <Label class="form-check-label" for="flexCheckDefault">
                    Remember me
                  </Label>
                </div>
              </Col>
              <Col lg={12} class="mt-3 mb-4">
                <Button color="primary" class="w-100">Sign in</Button>
              </Col>
              <div class="txet-center">
                <p class="mb-0 mt-2 text-center">
                  <Link to="password_forget" class="text-dark fw-bold"
                    >Forgot your password ?</Link
                  >
                </p>
              </div>
            </Row>
            <!-- end row -->
          </Form>
          <!-- end form -->
        </div>
        <div class="text-center mt-3">
          <p>
            <small class="text-white me-2">Don't have an account ?</small>
            <Link to="signup" class="text-white fw-bold">Create an account</Link
            >
          </p>
        </div>
      </Col>
    </Row>
  </Container>
</section>

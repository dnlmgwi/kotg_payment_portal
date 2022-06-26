<script>
  import { Input, Container, Row, Button, Form, Col } from "sveltestrap";
  import { Link } from "svelte-routing";
</script>

<section class="bg-login d-flex align-items-center">
  <Container>
    <Row class="justify-content-center mt-4">
      <Col lg={4}>
        <div class="bg-white p-4 mt-5 rounded">
          <div class="text-center">
            <h4 class="fw-bold mb-3">Globing</h4>
          </div>
          <Form class="login-form">
            <Row>
              <Col lg={12} class="mt-2">
                <Input
                  type="text"
                  class="form-control"
                  placeholder="First Name"
                  required=""
                />
              </Col>
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
                  <label class="form-check-label" for="flexCheckDefault">
                    I Accept <Link to="#">Terms And Condition</Link>
                  </label>
                </div>
              </Col>
              <Col lg={12} class="mt-4">
                <Button color="primary" class="w-100">Register</Button>
              </Col>
            </Row>
            <!-- end row -->
          </Form>
          <!-- end form -->
        </div>
        <div class="text-center mt-3">
          <p>
            <small class="text-white me-2">Already have an account ?</small>
            <Link to="login" class="text-white fw-bold">Sign in</Link>
          </p>
        </div>
      </Col>
    </Row>
  </Container>
</section>

<script>
  import {
    Input,
    Container,
    Row,
    Button,
    Form,
    ButtonGroup,
    Col,
    FormGroup,
    Label,
  } from "sveltestrap";
  import { Link } from "svelte-routing";
  import Footer from "../Components/Footer.svelte";
  let radioGroup;
</script>

<section class="bg-login d-flex align-items-center">
  <Container>
    <Row class="justify-content-center mt-4">
      <Col lg={4}>
        <div class="bg-white p-4 mt-5 rounded">
          <div class="text-center">
            <h4 class="fw-bold mb-3">Payment Portal</h4>
          </div>
          <FormGroup class="login-form">
            <Row>
              <Col lg={12} class="mt-2">
                <Input
                  type="text"
                  class="form-control"
                  placeholder="Ticket Reference"
                  required=""
                  oninvalid="setCustomValidity('Please enter valid Reference. ')"
                />
              </Col>
              <Col lg={12} class="mt-2">
                <Input
                  class="form-control"
                  placeholder="Phone Number"
                  required=""
                  type="tel"
                  id="phone"
                  oninvalid="setCustomValidity('Please enter valid Phone Number. ')"
                  pattern="[0-9]{(11, 14)}"
                />
              </Col>
              <!-- <Col lg={12} class="mt-2">
                <Input
                  type="password"
                  class="form-control"
                  placeholder="Password"
                  required=""
                />
              </Col> -->
              <!-- TODO Add Captcha -->
              <Col lg={12} class="mt-2">
                <div class="form-check">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    value=""
                    id="flexCheckDefault"
                  />
                  <label class="form-check-label" for="flexCheckDefault">
                    I declare I am over 18 years old and agree to KOTG's <Link
                      to="#">Terms And Condition</Link
                    >
                  </label>
                </div>
              </Col>
              <Col lg={12} class="mt-5">
                <Button color="primary" class="w-100">Pay</Button>
              </Col>
            </Row>
            <!-- end row -->
          </FormGroup>
          <!-- end form -->
        </div>
        <div class="text-center mt-3">
          <p>
            <small class="text-white me-2">v0.0.1</small>
          </p>
        </div>
      </Col>
    </Row>
    <Footer />
  </Container>
</section>

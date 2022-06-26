<script>
  import {
    Input,
    Container,
    Row,
    Button,
    Form,
    Col,
    Spinner,
  } from "sveltestrap";

  import Footer from "../Components/Footer.svelte";
  import { Link, navigate } from "svelte-routing";

  let loading = false;
  let todos = [];

  const initPayment = async () => {
    loading = true;
    const response = await fetch("https://jsonplaceholder.typicode.com/todos");
    todos = await response.json();

    if (response.ok) {
      loading = false;
    } else {
      throw new Error(text);
    }
  };

  function onSubmit() {
    initPayment().then(() => {
      navigate("/payment-success", { replace: true });
    });
  }
</script>

<section class="bg-login d-flex align-items-center">
  <Container>
    <Row class="justify-content-center mt-5">
      <Col lg={4}>
        <div class="mt-2" />
        <img
          src="assets/logo.png"
          alt=""
          class="img-fluid mx-auto mt-5 d-block"
        />
        <div class="bg-white p-4 mt-5 rounded">
          {#if loading === true}
            <Row class="justify-content-center mt-5"><Spinner primary /></Row>
          {:else}
            <div class="text-center">
              <h4 class="fw-bold mb-3">Payment Portal</h4>
            </div>
            <Form class="login-form">
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
                <!-- <captcha sitekey={mySitekey} /> -->
                <!-- TODO Add Captcha -->
                <Col lg={12} class="mt-2">
                  <div class="form-check">
                    <input
                      class="form-check-input"
                      type="checkbox"
                      value=""
                      id="flexCheckDefault"
                    />
                    <p>
                      <label class="form-check-label" for="flexCheckDefault">
                        I declare I am over 18 years old and agree to KOTG's <Link
                          to="#">Terms And Condition</Link
                        ></label
                      >
                    </p>
                  </div>
                </Col>
                <Col lg={12} class="mt-5">
                  <Button on:click={onSubmit} color="primary" class="w-100"
                    >Pay</Button
                  >
                </Col>
              </Row>
              <!-- end row -->
            </Form>

            <!-- end form -->
          {/if}
        </div>
        <div class="text-center mt-3">
          <p>
            <small class="me-2">v0.0.5-alpha</small>
          </p>
        </div>
      </Col>
    </Row>
    <Footer />
  </Container>
</section>

<style>
  img {
    width: 110px;
  }
</style>

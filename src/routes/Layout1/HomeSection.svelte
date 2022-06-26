<script>
  import {
    Button,
    Container,
    Row,
    Col,
    Label,
    Input
  } from 'sveltestrap'

</script>

<section class="section bg-home" id="home">
  <div class="home-center">
    <div class="home-desc-center">
      <Container>
        <Row class="vertical-content">
          <Col lg={7}>
            <div>
              <h1 class="text-white home-title mb-0">
                Create amazing landing page with globing template
              </h1>
              <p class="text-muted home-subtitle mt-4 mb-0">
                It is a long established fact that a reader will be of a page
                when established fact looking at its layout. Maecenas class
                semper class semper sollicitudin lectus lorem iaculis imperdiet
                aliquam.
              </p>
              <div class="mt-4">
                <a href={"#"} class="btn btn-outline-white btn-round">Read More</a
                >
              </div>
            </div>
          </Col>
          <!-- end col -->
          <Col lg={5} class="mt-3">
            <div class="home-registration-form mx-auto bg-white w-75 p-4">
              <h5 class="form-title mb-4 text-center fw-bold">
                Get 30 days FREE Trial
              </h5>
              <form class="registration-form">
                <Label class="text-muted">First Name</Label>
                <Input
                  type="text"
                  id="exampleInputName1"
                  class="form-control mb-2 registration-input-box"
                />
                <Label class="text-muted">Email</Label>
                <Input
                  type="email"
                  id="exampleInputEmail1"
                  class="form-control mb-2 registration-input-box"
                />
                <Label class="text-muted">Password</Label>
                <Input
                  type="password"
                  id="password1"
                  class="form-control mb-2 registration-input-box"
                />
                <Button color="primary" class="w-100 mt-3 text-uppercase"
                  >Get Started</Button>
              </form>
              <!-- end form -->
            </div>
          </Col>
          <!-- end col -->
        </Row>
        <!-- end row -->
      </Container>
    </div>
  </div>
</section>

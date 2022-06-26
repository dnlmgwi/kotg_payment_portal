<script>
  import { Form, Row, Col, Input, Container } from 'sveltestrap'
  export let contactData = {}
  let {
    heading,
    boldheading,
    description,
    customercare,
    officeaddress,
    emailaddress,
    officetime
  } = contactData
</script>

<section class="section" id="contact">
  <Container>
    <Row class="justify-content-center text-center">
      <Col lg={12}>
        <i class="ti-headphone-alt title-icon text-muted" />
        <h3 class="title">
          {heading} <span class="fw-bold">{boldheading}</span>
        </h3>
        <p class="text-muted mt-3 title-subtitle mx-auto">
          {description}
        </p>
      </Col>
      <!-- end col -->
    </Row>
    <!-- end row -->
    <Row>
      <Col lg={4}>
        <div class="mt-4 pt-4">
          <p class="text-muted mt-4">
            <span class="fw-bold ">Customer care:</span><br />
            <span class="d-block mt-2">{customercare}</span>
          </p>
          <p class="text-muted mt-4">
            <span class="fw-bold ">Office Address:</span><br />
            <span class="d-block mt-2">{officeaddress}</span>
          </p>
          <p class="text-muted mt-4">
            <span class="fw-bold ">Email Address:</span><br />
            <span class="d-block mt-2">{emailaddress}</span>
          </p>
          <p class="text-muted mt-4">
            <span class="fw-bold ">Office Time:</span><br />
            <span class="d-block mt-2">{officetime}</span>
          </p>
        </div>
      </Col>
      <!-- end col -->
      <Col lg={8}>
        <div class="custom-form mt-4 pt-4">
          <Form method="post" name="myForm">
            <p id="error-msg" />
            <div id="simple-msg" />
            <Row>
              <Col lg={6}>
                <div class="form-group mt-2">
                  <Input
                    name="name"
                    id="name"
                    type="text"
                    class="form-control"
                    placeholder="Your name*"
                  />
                </div>
              </Col>
              <!-- end col -->
              <Col lg={6}>
                <div class="form-group mt-2">
                  <Input
                    name="email"
                    id="email"
                    type="email"
                    class="form-control"
                    placeholder="Your email*"
                  />
                </div>
              </Col>
              <!-- end col -->
            </Row>
            <!-- end row -->
            <Row>
              <Col lg={12}>
                <div class="form-group mt-2">
                  <Input
                    type="text"
                    class="form-control"
                    id="subject"
                    placeholder="Your Subject.."
                  />
                </div>
              </Col>
              <!-- end col -->
            </Row>
            <!-- end row -->
            <Row>
              <Col lg={12}>
                <div class="form-group mt-2">
                  <Input
                    type="text"
                    name="comments"
                    id="comments"
                    rows="4"
                    class="form-control"
                    placeholder="Your message..."
                  />
                </div>
              </Col>
              <!-- end col -->
            </Row>
            <!-- end row -->
            <Row>
              <Col lg={12} class="text-end">
                <Input
                  type="submit"
                  id="submit"
                  name="send"
                  class="submitBnt btn btn-primary"
                  value="Send Message"
                />
                <div id="simple-msg" />
              </Col>
              <!-- end col -->
            </Row>
            <!-- end row -->
          </Form>
          <!-- end form -->
        </div>
      </Col>
      <!-- end col -->
    </Row>
    <!-- end row -->
  </Container>
  <!-- end container -->
</section>

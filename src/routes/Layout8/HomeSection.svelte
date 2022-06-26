<script>
  import { Container, Row, Col } from "sveltestrap";
  import { Link } from "svelte-routing";
</script>

<section class="section bg-gradient half-home" id="home">
  <div class="home-center">
    <div class="home-desc-center">
      <Container>
        <Row class="justify-content-center">
          <Col lg={10}>
            <div class="text-center">
              <h1 class="text-white home-title mb-0">
                A digital web studio creating stunning & engaging online
                experiences
              </h1>
              <p
                class="text-white home-subtitle-center home-subtitle mt-4 mb-0 mx-auto"
              >
                It is a long established fact that a reader will be of a page
                when established fact looking at its layout.
              </p>
              <div class="mt-4">
                <Link to={"#"} class="btn btn-outline-white btn-round"
                  >Read More</Link
                >
              </div>
            </div>
          </Col><!-- end col -->
        </Row><!-- end row -->
      </Container>
    </div>
  </div>
</section>
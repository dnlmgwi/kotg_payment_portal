<script>
  import { Container, Row, Col } from "sveltestrap";
  import { Link } from "svelte-routing";
  import Typewriter from "svelte-typewriter";
</script>

<section class="section bg-home half-home" id="home">
  <div class="home-center">
    <div class="home-desc-center">
      <Container>
        <Row class="justify-content-center">
          <Col lg={10}>
            <div class="text-center">
              <h1 class="text-white home-title mb-0">
                <Typewriter loop interval={50}>
                  <span class="element">
                    Professional Landing Page Template</span>
                  <span class="element"> We are Creative</span>
                  <span class="element"> We are Modern</span>
                </Typewriter>
              </h1>

              <p
                class="text-muted home-subtitle-center home-subtitle mt-4 mb-0 mx-auto"
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
          </Col>
          <!-- end col -->
        </Row>
        <!-- end row -->
      </Container>
    </div>
  </div>
</section>

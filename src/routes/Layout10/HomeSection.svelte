<script>
    import { Container, Row, Col } from 'sveltestrap'
    import { Link } from 'svelte-routing'
  </script>
<section class="section vh-100" id="home">
    <video autoplay muted loop id="myVideo">
        <source src="http://techslides.com/demos/sample-videos/small.mp4" type="video/mp4">
    </video>
    <div class="bg-overlay"></div>
    <div class="home-center">
        <div class="home-desc-center">
            <Container>
                <Row>
                    <Col lg={7}>
                        <div>
                            <h1 class="text-white home-title mb-0">We Love Make Things Amazing And Simple</h1>
                            <p class="text-muted home-subtitle mt-4 mb-0">It is a long established fact that a
                                reader will be of a page when established fact looking at its layout.</p>
                            <div class="mt-4">
                                <a href={"#"} class="btn btn-outline-white btn-round">Read More</a>
                            </div>
                        </div>
                    </Col><!-- end col -->
                </Row><!-- end row -->
            </Container>
        </div>
    </div>
</section>
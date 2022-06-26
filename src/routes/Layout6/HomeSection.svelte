<script>
  import { onMount } from "svelte";

  import { Container, Row, Col, Form, Input, Button } from "sveltestrap";

  //image-rotate
  var i = 0;
  var image_rotate = [];
  var time = 3000;

  image_rotate[0] = "assets/images/slide-1.jpg";
  image_rotate[1] = "assets/images/slide-2.jpg";
  image_rotate[2] = "assets/images/slide-3.jpg";

  onMount(() => {
    function changeimage() {
      document.silde.src = image_rotate[i];
      i = i < image_rotate.length - 1 ? i + 1 : 0;
      setTimeout(() => {
        changeimage();
      }, time);
    }

    changeimage();
  });
  
</script>

<section class="back-slide" id="home">
  <img name="silde" class="slide-img" src="" alt="demo" />
  <div class="bg-overlay" />
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
              <div class="text-center search-form mt-4">
                <Form action="#">
                  <Input type="text" placeholder="Email" />
                  <Button type="submit" color="primary">SubCribe</Button>
                </Form>
              </div>
            </div>
          </Col><!-- end col -->
        </Row><!-- end row -->
      </Container>
    </div>
  </div>
</section>

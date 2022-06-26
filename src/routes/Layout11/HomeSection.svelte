<script>
  import { onMount } from "svelte";
  import { Container, Row, Col } from "sveltestrap";
  import { Link } from "svelte-routing";

  //image-rotate
  var i = 0;
  var image_rotate = [];
  var text_rotate = [];
  var time = 3000;

  image_rotate[0] = "assets/images/slide-1.jpg";
  image_rotate[1] = "assets/images/slide-2.jpg";
  image_rotate[2] = "assets/images/slide-3.jpg";
  text_rotate[0] = "We love make things amazing and simple";
  text_rotate[1] = "Create amazing landing page with Globing";
  text_rotate[2] = "Perfact solution for small businesses";

  onMount(() => {
    function changeimage() {
      document.silde.src = image_rotate[i];
      document.getElementById("target").innerHTML = text_rotate[i];
      i = i < image_rotate.length - 1 ? i + 1 : 0;
      setTimeout(() => {
        changeimage();
      }, time);
    }

    changeimage();
  });
</script>

<section class="back-slide" id="home">
  <img name="silde" class="slide-img" alt="demo5" />
  <div class="bg-overlay" />
  <div class="home-center">
    <div class="home-desc-center">
      <Container>
        <Row class="justify-content-center">
          <Col lg={9}>
            <div class="text-center">
              <h1 class="home-title text-white text-rotate" id="target">
                &nbsp;
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

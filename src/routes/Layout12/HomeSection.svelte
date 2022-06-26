<script>
  import { Container, Row, Col } from "sveltestrap";

  import Carousel from "svelte-carousel";

  let carousel;

  import { Link } from "svelte-routing";

  const items = [
    {
      title: "We love make things amazing and simple",
      description:
        "It is a long established fact that a reader will be of a page when established fact looking at its layout.",
    },
    {
      title: "Create amazing landing page with Globing",
      description:
        "It is a long established fact that a reader will be of a page when established fact looking at its layout.",
    },
    {
      title: "Perfact solution for small businesses",
      description:
        "It is a long established fact that a reader will be of a page when established fact looking at its layout.",
    },
  ];

  let activeIndex = 0;
</script>

<section class="section bg-home half-home" id="home">
  <div class="home-center">
    <div class="home-desc-center">
      <Container>
        <Row class="justify-content-center">
          <Col lg={10}>
            <Carousel
              class="text-center home-carousel"
              bind:this={carousel}
              arrows={false}
              dots={true}
              let:showPrevPage
              let:showNextPage
            >
              {#each items as item}
                <div class="text-center">
                  <h1 class="text-white home-title mb-0">
                    <span class="text-rotate">{item.title}</span>
                  </h1>
                  <p
                    class="text-muted home-subtitle-center home-subtitle mt-4 mb-0 mx-auto"
                  >
                    {item.description}
                  </p>
                  <div class="mt-4 mb-4">
                    <Link to="#" class="btn btn-outline-white btn-round"
                      >Read More</Link
                    >
                  </div>
                </div>
              {/each}
            </Carousel>
          </Col>
        </Row>
      </Container>
    </div>
  </div>
</section>

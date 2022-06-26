<script>
  import { Container, Row, Col } from 'sveltestrap'
  import Carousel from 'svelte-carousel'
  import { Link } from 'svelte-routing'
  let carousel

  function goToPrevPage() {
    carousel.goToPrev({ animated: false })
  }

  function goToNextPage() {
    carousel.goToNext({ animated: false })
  }
  export let testimonialData = {}
  const { testimonial_list } = testimonialData
</script>

<section class="section bg-client" id="testi">
  <Container>
    <Row class="justify-content-center mt-5 mb-5">
      <Col lg={12}>
        <Carousel
          bind:this={carousel}
          arrows={false}
          dots={false}
          let:showPrevPage
          let:showNextPage
        >
          {#each testimonial_list as testimonial}
            <div>
              <div class="text-center w-75 mx-auto">
                <div class="testi-icon text-white">
                  <i class="ti-quote-left" />
                </div>
                <div class="mt-3">
                  <p class="user-review text-center">
                    {testimonial.description}
                  </p>
                  <div class="">
                    <img
                      src={testimonial.profile}
                      alt=""
                      class="rounded-circle testi-user mx-auto d-block"
                    />
                  </div>
                  <p class="testi-user-name text-center text-white mb-0 mt-4">
                    - {testimonial.name}
                  </p>
                  <p class="text-muted">
                    <span class="ti-star text-warning" />
                    <span class="ti-star text-warning" />
                    <span class="ti-star text-warning" />
                    <span class="ti-star text-warning" />
                    <span class="ti-star text-warning" />
                  </p>
                </div>
              </div>
            </div>
          {/each}
        </Carousel>
        <Link to={'#'} on:click={goToPrevPage}>
          <div class="test_nav_left owl-prev"><i class="ti-angle-left" /></div>
        </Link>

        <Link to={'#'} on:click={goToNextPage}>
          <div class="test_nav_right owl-nex"><i class="ti-angle-right" /></div>
        </Link>
      </Col>
    </Row>
  </Container>
</section>

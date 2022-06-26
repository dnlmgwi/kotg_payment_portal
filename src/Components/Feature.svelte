<script>
  import { Container, Row, Col } from 'sveltestrap'
  export let featureData = {}
  const { heading, boldheading, description, feature_list } = featureData
</script>

<section class="section bg-light" id="features">
  <Container>
    <Row class="justify-content-center text-center">
      <Col lg={12}>
        <i class="ti-bookmark-alt title-icon text-muted" />
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

    {#each feature_list as feature}
      <Row class="mt-5 vertical-content">
        <Col lg={6} class={feature.type == 'left' ? 'mt-2 order-lg-2' : 'mt-2'}>
          <div>
            <img src={feature.img} alt="" class="img-fluid mx-auto d-block" />
          </div>
        </Col>
        <!-- end col -->
        <Col
          lg={5}
          class={feature.type == 'left'
            ? 'mx-auto mt-2 order-lg-1'
            : 'offset-lg-1 mt-2'}
        >
          <div class="features-desc">
            <h2>{feature.title}</h2>
            <p class="text-muted mt-3">
              {feature.description}
            </p>
            <a href={'#'} class="btn btn-primary btn-round mt-3"
              >Read more<i class="mdi mdi-chevron-right" /></a
            >
          </div>
        </Col>
        <!-- end col -->
      </Row>
      <!-- end row -->
    {/each}
  </Container>
</section>

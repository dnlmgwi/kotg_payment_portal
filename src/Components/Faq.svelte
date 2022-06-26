<script>
  import { Container, Row, Col } from 'sveltestrap'
  export let faqData = {}
  export let ctaData = {}
  const { heading, boldheading, description, pricing_list } = faqData
  const { title, buttontext } = ctaData
</script>

<section class="section" id="faq">
  <Container>
    <Row class="justify-content-center text-center">
      <Col lg={12}>
        <i class="ti-comments title-icon text-muted" />
        <h3 class="title">
          {heading} <span class="fw-bold">{boldheading}</span> Center
        </h3>
        <p class="text-muted mt-3 title-subtitle mx-auto">
          {description}
        </p>
      </Col>
      <!-- end col -->
    </Row>
    <!-- end row -->
    <Row class="mt-5">
      {#each pricing_list as pricing}
        <Col lg={6}>
          <div class="ps-4 pe-4">
            {#each pricing.pricing1 as pricingdata}
              <div class="mt-4">
                <div>
                  <h5 class="mb-0 f-18 font-weight-600">
                    Q. {pricingdata.title}
                  </h5>
                </div>
                <div class="mt-3">
                  <p class="text-muted">
                    {pricingdata.description}
                  </p>
                </div>
              </div>
            {/each}
          </div>
        </Col>
      {/each}
      <!-- end col -->
    </Row>
    <!-- end row -->
  </Container>
</section>

<!-- START CTA -->
<section class="section">
  <Container>
    <Row>
      <Col lg={12}>
        <div class="text-center">
          <h3 class="mb-4">{title}</h3>
          <div class="">
            <a href={'#'} class="btn btn-round btn-primary">{buttontext}</a>
          </div>
        </div>
      </Col>
    </Row>
  </Container>
</section>

<script>
  import { Container, Row, Col } from 'sveltestrap'
  export let pricingData = {}
  const { heading, boldheading, description, pricing_list } = pricingData
</script>

<section class="section bg-light" id="pricing">
  <Container>
    <Row class="justify-content-center text-center">
      <div class="col-lg-12">
        <i class="ti-package title-icon text-muted" />
        <h3 class="title">
          {heading} <span class="fw-bold">{boldheading}</span>
        </h3>
        <p class="text-muted mt-3 title-subtitle mx-auto">
          {description}
        </p>
      </div>
    </Row>
    <Row class="mt-5">
      {#each pricing_list as pricing}
        <Col lg={4}>
          <div class="bg-white price-box text-center mt-3">
            <div class="plan-price fw-bold">
              <h1 class="mb-0 fw-bold">{pricing.price}</h1>
              <p class="mb-0">Per Month</p>
            </div>
            <div class="plan-features text-muted mt-5 mb-5">
              <p>Bandwidth: <b class="text-primary">{pricing.bandwidth}</b></p>
              <p>Onlinespace: {pricing.onlinespace}</p>
              <p>Support: {pricing.support}</p>
              <p>{pricing.domain} Domain</p>
              <p class="mb-0">{pricing.hiddenfees}</p>
            </div>
            <div>
              <a href={'#'} class="btn btn-primary btn-round">Join Now</a>
            </div>
          </div>
        </Col>
      {/each}
    </Row>
  </Container>
</section>

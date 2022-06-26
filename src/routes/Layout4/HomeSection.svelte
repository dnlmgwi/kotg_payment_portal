<script>
  import { Container, Row, Col } from 'sveltestrap'
  import { Link } from 'svelte-routing'
  import { onMount } from 'svelte';

  const text_rotate = new Array(
		'We love make things amazing and simple',
		'Create amazing landing page with Globing',
		'Perfact solution for small businesses'
	);

    onMount(() => {
		let i = 0;
		function changeText() {
			document.getElementById('target').innerHTML = text_rotate[i];
			i = i < text_rotate.length - 1 ? i + 1 : 0;
			setTimeout(() => {
				changeText();
			}, 3000);
		}

		changeText();
	});

</script>

<section class="section bg-home half-home" id="home">
  <div class="home-center">
    <div class="home-desc-center">
      <Container>
        <Row class="justify-content-center">
          <Col lg={10}>
            <div class="text-center">
              <h1 class="home-title text-white text-rotate" id="target">.</h1>
              <p
                class="text-muted home-subtitle-center home-subtitle mt-4 mb-0 mx-auto"
              >
                It is a long established fact that a reader will be of a page
                when established fact looking at its layout.
              </p>
              <div class="mt-4">
                <Link to={'#'} class="btn btn-outline-white btn-round"
                  >Read More</Link
                >
              </div>
            </div>
          </Col>
          <!-- end col -->
        </Row>
        <!-- end row -->
      </Container>
      <!-- end container -->
    </div>
  </div>
</section>

<!-- Navbar component -->
<script>

  import { scrollto } from 'svelte-scrollto'
  import { onMount } from 'svelte'
  import { Button } from "sveltestrap";

  function windowScroll() {
    const navbar = document.getElementById("navbar");
    if (
        document.body.scrollTop >= 50 ||
        document.documentElement.scrollTop >= 50
    ) {
        navbar.classList.add("nav-sticky");
    } else {
        navbar.classList.remove("nav-sticky");
    }

    if (
        document.body.scrollTop > 100 ||
        document.documentElement.scrollTop > 100
    ) {
        // document.getElementById("back-to-top").style.display = "inline";
    } else {
        // document.getElementById("back-to-top").style.display = "none";
    }
}

window.addEventListener('scroll', (ev) => {
    ev.preventDefault();
    windowScroll();
})

  /**
   * Toggle menu
   */
  const toggleMenu = () => {
    document.getElementById('navbarCollapse').classList.toggle('show')
  }

  /**
   * Component mount
   */
  onMount(() => {
    var section = document.querySelectorAll('.common-section')

    var sections = {}
    var i = 0

    Array.prototype.forEach.call(section, function (e) {
      sections[e.id] = e.offsetTop
    })

    window.onscroll = function () {
      var scrollPosition =
        document.documentElement.scrollTop || document.body.scrollTop
      for (i in sections) {
        if (sections[i] <= scrollPosition) {
          document.querySelector('.active').setAttribute('class', ' ')
          document
            .querySelector('a[href*=' + i + ']')
            .setAttribute('class', 'active')
        }
      }
    }
  })

  /**
   * Scroll method
   */
  const handleScroll = () => {
    var navbar = document.getElementById('navbar')
    if (
      document.body.scrollTop > 50 ||
      document.documentElement.scrollTop > 50
    ) {
      navbar.classList.add('is-sticky')
    } else {
      navbar.classList.remove('is-sticky')
    }
  }

  window.addEventListener('scroll', handleScroll, { passive: false })

  export let extraclass;
  
</script>

<!-- STRAT NAVBAR -->
<div>
  <nav
    class={"navbar navbar-expand-lg fixed-top navbar-custom sticky sticky-dark " + extraclass}
    id="navbar"
  >
    <div class="container">
      <a class="navbar-brand" href={"#"}>Globing</a>

      <Button class="navbar-toggler" on:click={toggleMenu}>
        <span class="ti-menu" />
      </Button>

      <div class="collapse navbar-collapse" id="navbarCollapse">
        <ul class="navbar-nav mx-auto" id="navbar-navlist">
          <li class="nav-item">
            <a class="nav-link" use:scrollto={"#home"} href={"#home"}>Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" use:scrollto={"#services"} href={"#services"}>Services</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" use:scrollto={"#features"} href={"#features"}>Features</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" use:scrollto={"#testi"} href={"#testi"}>Client</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" use:scrollto={"#team"} href={"#team"}>Team</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" use:scrollto={"#faq"} href={"#faq"}>FAQ</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" use:scrollto={"#pricing"} href={"#pricing"}>Pricing</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" use:scrollto={"#contact"} href={"#contact"}>Contact</a>
          </li>
        </ul>
        <!-- end ul -->
        <div>
          <ul class="text-end list-unstyled list-inline mb-0 nav-social">
            <li class="list-inline-item text-white nav-number">
              <i class="ti-mobile" /> <span>+1 234 567 789</span>
            </li>
            <li class="list-inline-item">
              <a href={"#"} class="facebook"><i class="ti-facebook" /></a>
            </li>
          </ul>
          <!-- end ul -->
        </div>
      </div>
    </div>
  </nav>
</div>
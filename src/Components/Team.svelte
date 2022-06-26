<script>
  export let teamData = {}
  const { heading, boldheading, description, team_list } = teamData
</script>

<section class="section bg-light" id="team">
  <div class="container">
    <div class="row justify-content-center text-center">
      <div class="col-lg-12">
        <i class="ti-user title-icon text-muted" />
        <h3 class="title">
          {heading} <span class="fw-bold">{boldheading}</span>
        </h3>
        <p class="text-muted mt-3 title-subtitle mx-auto">{description}</p>
      </div>
      <!-- end col -->
    </div>
    <!-- end row -->
    <div class="row mt-5">
      {#each team_list as team}
        <div class="col-lg-4">
          <div class="text-center bg-white team-box mt-3 p-5">
            <div>
              <img
                src={team.profile}
                alt=""
                class="img-fluid rounded-circle mx-auto d-block"
              />
            </div>
            <div class="team-name">
              <p class="fw-bold mb-0 mt-4">{team.name}</p>
              <p class="text-muted mt-4">
                {team.designation}
              </p>
            </div>
            <div>
              <ul class="list-inline team-social mt-4 mb-0">
                <li class="list-inline-item">
                  <a href={'#'}><i class="ti-github" /></a>
                </li>
                <li class="list-inline-item">
                  <a href={'#'}><i class="ti-skype" /></a>
                </li>
                <li class="list-inline-item">
                  <a href={'#'}><i class="ti-twitter-alt" /></a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      {/each}
    </div>
    <!-- end row -->
  </div>
</section>

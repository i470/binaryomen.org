<template>
  <div class="container">
    <div class="col-lg-12 text-algin-center">
      <vue-typed-js :strings="['WELCOME TO ^1000 CRYPTO DEVELOPER']">
        <h1 class="typing"></h1>
      </vue-typed-js>
      <h2>Bitcoin, Ethereum and other Cryptocurrency Services</h2>
    </div>
    <div class="row">
      <div class="col-lg-4 col-sm-12">
        <div class="card" style="width: 18rem;">
          <img src="img/block.png" class="card-img-top" alt="binaryOmen" />
          <div class="card-body">
            <h4 class="card-title">Technical Support</h4>
            <p class="card-text">
              We have years of experience with Bitcoin mining and payment systems to put behind you.
              Set up your mining rigs or integrate Bitcoin payments into your business with top of the line support.
            </p>
          </div>
        </div>
      </div>
      <div class="col-lg-4 col-sm-12">
        <div class="card" style="width: 18rem;">
          <img src="img/spaceship.jpg" class="card-img-top" alt="binaryOmen" />
          <div class="card-body">
            <h4 class="card-title">In-Person Or Remote Consultation</h4>
            <p class="card-text">
              Quick, reliable service available in person, by telephone or Skype worldwide.
              We offer consultation for beginners on account setup, wallet security, research,
              and any general questions you might have about cryptocurrency.
            </p>
          </div>
        </div>
      </div>
      <div class="col-lg-4 col-sm-12">
        <div class="card" style="width: 18rem;">
          <img src="img/fred_g_07.jpg" class="card-img-top" alt="binaryOmen" />
          <div class="card-body">
            <h4 class="card-title">Code and ICO</h4>
            <p class="card-text">
              If you're looking to start your own crypto projectm realease your own crypto currency or find help
              for an existing one, we offer expertise to get you on track. We can review code, give project guidance
              and connect you with other crypto professionals to help build your team.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
</script>
<style>
.navbar-nav .nav-item p {
  line-height: inherit;
  margin-left: 5px;
}

.carouselWrapper {
  position: absolute;
  top: 0;
  left: 0;
}

.card-title {
  color: #e14eca !important;
}
</style>
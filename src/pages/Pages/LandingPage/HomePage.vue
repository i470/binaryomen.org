<template>
  <div class="wrapHomePage">
    <div class="container text-style">
      <div class="col-lg-12">
        <vue-typed-js
          :strings="['WELCOME TO ^1000 CRYPTO DEVELOPER']"
          :loop="true"
          :typeSpeed="60"
          :backSpeed="40"
          :showCursor="true"
          :cursorChar="'____'"
        >
          <h1 class="typing justify-content-center"></h1>
        </vue-typed-js>
        <h2 class="justify-content-center">Bitcoin, Ethereum and other Cryptocurrency Services</h2>
      </div>
      <div class="row">
        <div class="col-lg-4 col-sm-12 d-flex justify-content-center">
          <div class="card">
            <img src="img/energy.jpg" class="card-img-top" alt="binaryOmen" />
            <div class="card-body">
              <h4 class="card-title">Technical Support</h4>
              <p class="card-text">
                We have years of experience with Bitcoin mining and payment systems to put behind you.
                Set up your mining rigs or integrate Bitcoin payments into your business with top of the line support.
              </p>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-sm-12 d-flex justify-content-center">
          <div class="card card-text-wrapp">
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
        <div class="col-lg-4 col-sm-12 d-flex justify-content-center">
          <div class="card">
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
    <div class="container-fluid mt-5">
      <img src="img/space_inavder_binary_omen.png" class="show" alt="space_inavder_binary_omen" />
      <div class="col-lg-10 col-md-12 d-flex justify-content-start">
        <div class="media">
          <div class="media-body card-titley">
            <h3 class="mt-0 mb-1 card-title">Cloud Computing</h3>Our IT solutions carve the path for organizations to modernize infrastructure and optimize workflow
            like never before. This service provides a wide variety of technological capabilities to boost
            efficiencies, enhance security and allow infinite scalability for future growth. With this
            resource and our expertise, we’ll help maximize your organization’s productivity.
          </div>
          <img
            src="img/space_inavder_binary_omen.png"
            class="ml-3 show-2 justify-content-center"
            alt="space_inavder_binary_omen"
          />
        </div>
      </div>
    </div>
    <div class="container-fluid mt-5">
      <img src="img/space_inavder_binary_omen.png" class="show show-color" alt="space_inavder_binary_omen" />
      <div class="col-lg-10 col-md-12 d-flex justify-content-end ml-auto">
        <div class="media">
          <img
            src="img/space_inavder_binary_omen.png"
            class="align-self-start mr-3 show-2 justify-content-center"
            alt="space_inavder_binary_omen"
          />
          <div class="media-body">
            <h3 class="mt-0 card-title">Security</h3>In today’s hyperconnected world, organizations are challenged in more ways than ever to stay ahead of the curve.
            This comprehensive service is designed to fit your unique needs without disrupting productivity or workflow. With our
            end-to-end solutions, cryptodeveloper is sure to help your organization succeed.
          </div>
        </div>
      </div>
    </div>
    <div class="container-fluid mt-5">
      <img src="img/space_inavder_binary_omen.png" class="show" alt="space_inavder_binary_omen" />
      <div class="col-lg-10 col-md-12 d-flex justify-content-start">
        <div class="media">
          <div class="media-body">
            <h3 class="mt-0 mb-1 card-title">Mobility</h3>Enabling your workforce with top-notch technologies isn’t just important, but imperative for business success.
            This customizable solution allows your team to work seamlessly and collaboratively in a protected space. No matter what
            IT services you need, cryptodeveloper will be there to support you every step of the way.
          </div>
          <img
            src="img/space_inavder_binary_omen.png"
            class="ml-3 show-2 justify-content-center"
            alt="space_inavder_binary_omen"
          />
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

.text-style {
  font-family: "Press Start 2P", cursive !important;
}

p.card-text {
  z-index: 2200 !important;
}

.show {
  display: none;
}

.wrapHomePage {
  margin-bottom: 12rem;
}

img:nth-child(even) {
  background: #fff;
}
.show-2:nth-child(odd) {
  background: red;
}

@media screen and (max-width: 600px) {
  h1 {
    font-size: 24px;
  }

  h2 {
    font-size: 18px;
  }

  h3 {
    text-align: center;
  }
  .media-body {
    text-align: center;
  }

  .card-wrapp,
  .card-img {
    height: 60vh;
  }

  .card-img {
    width: 120vw;
  }

  .show {
    display: block;
    margin-bottom: 1rem;
    margin-left: auto;
    margin-right: auto;
    
  }

  img.show-color {
    background: red !important;
  }

  .show:nth-child(odd) {
    background: #fff;
  }

  .show-2 {
    display: none;
  }

  .wrapHomePage {
    margin-bottom: 14rem;
  }
}
</style>
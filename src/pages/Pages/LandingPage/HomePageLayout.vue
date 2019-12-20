<template>
  <div>
    <base-nav
      v-model="showMenu"
      type="white"
      :transparent="true"
      menu-classes="justify-content-end"
      class="auth-navbar fixed-top"
    >
    
      <div slot="brand" class="navbar-wrapper">
        <a class="navbar-brand" href="/Home">Cryptodeveloper</a>
      </div>
      <!--
      <ul class="navbar-nav">
        <router-link class="nav-item" tag="li" to="/dashboard">
          <a class="nav-link text-primary">
            <i class="tim-icons icon-minimal-left"></i> Back to Dashboard
          </a>
        </router-link>
        <router-link class="nav-item" tag="li" to="/login">
          <a class="nav-link">
            <i class="tim-icons icon-single-02"></i> Login
          </a>
        </router-link>

        <router-link class="nav-item" tag="li" to="/pricing">
          <a class="nav-link"> <i class="tim-icons icon-coins"></i> Pricing </a>
        </router-link>

        <router-link class="nav-item" tag="li" to="/lock">
          <a class="nav-link">
            <i class="tim-icons icon-lock-circle"></i> Lock
          </a>
        </router-link>
      </ul>-->
    </base-nav>
    

    <div class="wrapper wrapper-full-page">
     <img src="img/card-primary.png" alt="binaryomen" class="imgWrapperTopRight"/>
      <div class="full-page" :class="pageClass">
        <div class="content">
          <zoom-center-transition :duration="pageTransitionDuration" mode="out-in">
            <router-view></router-view>
          </zoom-center-transition>
        </div> 
        <footer class="footer">
          <div class="container-fluid">
            <img src="img/card-primary.png" alt="binaryomen" class="imgWrapperBottom"/>
              <h4>Address:</h4>
              <p>
                333 N Pennington Dr
                Chandler, 85224
                USA
              </p>
              <h4 class="mt-3">Contact:</h4>
              <p>ingamx@gmail.com</p>
            
            <nav>
              <ul class="nav">
                <li class="nav-item">
                  <a
                    href="https://www.facebook.com/"
                    target="_blank"
                    rel="noopener"
                    class="nav-link"
                  ><i class="fab fa-facebook" style="font-size:24px"></i></a>
                </li>
                <li class="nav-item">
                  <a
                    href="http://www.twitter.com"
                    target="_blank"
                    rel="noopener"
                    class="nav-link"
                  ><i class="fab fa-twitter-square" style="font-size:24px"></i></a>
                </li>
                <li class="nav-item">
                  <a
                    href="http://www.linkedin.com"
                    target="_blank"
                    rel="noopener"
                    class="nav-link"
                  ><i class="fab fa-linkedin" style="font-size:24px"></i></a>
                </li>
              </ul>
            </nav>
            <div class="copyright">&copy; {{ year }}, made by cryptodeveloper</div>
          </div>
        </footer>
      </div>
    </div>
  </div>
</template>
<script>
import { BaseNav } from "src/components";
import { ZoomCenterTransition } from "vue2-transitions";

export default {
  components: {
    BaseNav,
    ZoomCenterTransition
  },
  props: {
    backgroundColor: {
      type: String,
      default: "black"
    }
  },
  data() {
    return {
      showMenu: false,
      menuTransitionDuration: 250,
      pageTransitionDuration: 200,
      year: new Date().getFullYear(),
      pageClass: "login-page"
    };
  },

  methods: {},
  beforeRouteUpdate(to, from, next) {
    // Close the mobile menu first then transition to next page
    if (this.showMenu) {
      this.closeMenu();
      setTimeout(() => {
        next();
      }, this.menuTransitionDuration);
    } else {
      next();
    }
  },
  mounted() {},
  watch: {}
};
</script>
<style lang="scss">
.navbar.auth-navbar {
  top: 0;
}

$scaleSize: 0.8;
@keyframes zoomIn8 {
  from {
    opacity: 0;
    transform: scale3d($scaleSize, $scaleSize, $scaleSize);
  }
  100% {
    opacity: 1;
  }
}

.wrapper-full-page .zoomIn {
  animation-name: zoomIn8;
}

.wrapper-full-page .zoomOut {
  animation-name: zoomOut8;
}

.imgWrapperBottom {
    height: 100%;
    border-radius: 0;
    z-index: -1;
    transform: rotateX(180deg);
    position: absolute;
	bottom: 0%;
	left: 0;
}
.imgWrapperTopRight {
   max-height: 35%;
    max-width: 35%;
    border-radius: 0;
    z-index: 11;
    transform: rotateY(180deg);
    position: absolute;
	top: 0%;
	right: 0;
}


</style>

<template>
<footer class="footer has-cards" id="contatti">
  <div class="container">
    <div class="row row-grid align-items-center my-md fade-in">
      <div class="col-lg-6">
        <h3 class="text-primary font-weight-light mb-2">Contatti</h3>
        <h4 class="mb-0 font-weight-light">Telefono: +39 327 183 5746</h4>
        <h4 class="mb-0 font-weight-light">E-mail: birladionut@yahoo.it</h4>
      </div>
      <div class="col-lg-6 text-lg-center btn-wrapper">
        <a target="_blank" rel="noopener" href="https://www.linkedin.com/in/ionut-birlad-59a069151/" class="btn btn-neutral btn-icon-only btn-facebook btn-lg btn-round" data-toggle="tooltip" data-original-title="Follow us">
          <i class="fa fa-linkedin-square" aria-hidden="true"></i>
        </a>
        <a target="_blank" rel="noopener" href="https://github.com/ionutbirlad" class="btn btn-neutral btn-icon-only btn-github btn-round btn-lg" data-toggle="tooltip" data-original-title="Star on Github">
          <i class="fa fa-github"></i>
        </a>
      </div>
    </div>

    <hr>

    <div class="row align-items-center justify-content-md-between">
      <div class="col-md-6">
        <div class="copyright">
          &copy; {{year}}
          <a href="https://www.linkedin.com/in/ionut-birlad-59a069151/" target="_blank" rel="noopener">Ionut Birlad</a> & <a href="https://www.creative-tim.com" target="_blank" rel="noopener">Creative Tim</a>
        </div>
      </div>
      <div class="col-md-6">
        <ul class="nav nav-footer justify-content-end">
          <li class="nav-item">
            <a href="https://github.com/creativetimofficial/argon-design-system/blob/master/LICENSE.md" class="nav-link" target="_blank" rel="noopener">MIT License</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</footer>
</template>

<script scoped>
export default {
  name: 'app-footer',
  data() {
    return {
      year: new Date().getFullYear()
    }
  },
  mounted() {
    // faders effect
    const faders = document.querySelectorAll(".fade-in");

    const appearOptions = {
      threshold: 0,
      rootMargin: "0px 0px -150px 0px"
    };

    const appearOnScroll = new IntersectionObserver(function(
        entries,
        appearOnScroll
      ) {
        entries.forEach(entry => {
          if (!entry.isIntersecting) {
            return;
          } else {
            entry.target.classList.add("appear");
            appearOnScroll.unobserve(entry.target);
          }
        });
      },
      appearOptions);

    faders.forEach(fader => {
      appearOnScroll.observe(fader);
    });
  }
};
</script>

<style lang="scss" scoped>
// fade in
.fade-in {
    opacity: 0;
    transition: opacity 250ms ease-in;
    &.appear {
        opacity: 1;
    }
}
</style>

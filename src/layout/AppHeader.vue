<template>
<header class="header-global">
  <base-nav class="navbar-main" transparent type="" effect="light" expand>
    <router-link slot="brand" class="navbar-brand mr-lg-5" to="/">
      <img id="logo" src="img/brand/me.png" alt="logo">
    </router-link>

    <div class="row" slot="content-header" slot-scope="{closeMenu}">
      <div class="col-6 collapse-brand">
        <router-link slot="brand" class="navbar-brand mr-lg-5" to="/">
          <img src="img/brand/me.png">
        </router-link>
      </div>
      <div class="col-6 collapse-close">
        <close-button @click="closeMenu"></close-button>
      </div>
    </div>
    <ul class="navbar-nav navbar-nav-hover align-items-lg-center ml-lg-auto">
      <li class="nav-item" @click="scrollToElement('chisono')">
        <a class="nav-link nav-link-icon">
          Chi sono
        </a>
      </li>
      <li class="nav-item" @click="scrollToElement('competenze')">
        <a class="nav-link nav-link-icon">
          Competenze
        </a>
      </li>
      <li class="nav-item dropdown">
        <base-dropdown class="nav-item" menu-classes="dropdown-menu-xl" tag="li" title="Progetti">
          <div class="dropdown-menu-inner">
            <a @click="scrollToElement('progetti')" class="media d-flex align-items-center">
              <div class="icon icon-shape bg-gradient-primary rounded-circle text-white">
                <i class="ni ni-spaceship"></i>
              </div>
              <div class="media-body ml-3">
                <h6 class="heading text-primary mb-md-1">Progetti Principali</h6>
                <p class="description d-none d-md-inline-block mb-0">Visualizza i principali progetti da me realizzati</p>
              </div>
            </a>
            <a href="https://github.com/ionutbirlad" target="_blank" rel="noopener noreferrer" class="media d-flex align-items-center">
              <div class="icon icon-shape bg-gradient-warning rounded-circle text-white">
                <i class="ni ni-ui-04"></i>
              </div>
              <div class="media-body ml-3">
                <h5 class="heading text-warning mb-md-1">Tutti i progetti</h5>
                <p class="description d-none d-md-inline-block mb-0">Guarda tutti i progetti che ho prodotto</p>
              </div>
            </a>
          </div>
        </base-dropdown>
      </li>
      <li class="nav-item" @click="scrollToElement('formazione')">
        <a class="nav-link nav-link-icon">
          Formazione
        </a>
      </li>
      <li class="nav-item" @click="scrollToElement('certificazioni')">
        <a class="nav-link nav-link-icon">
          Certificazioni
        </a>
      </li>
      <li class="nav-item" @click="scrollToElement('contatti')">
        <a class="nav-link nav-link-icon">
          Contatti
        </a>
      </li>
    </ul>
  </base-nav>
</header>
</template>

<script>
import BaseNav from "@/components/BaseNav";
import BaseDropdown from "@/components/BaseDropdown";
import CloseButton from "@/components/CloseButton";

export default {
  components: {
    BaseNav,
    CloseButton,
    BaseDropdown
  },
  methods: {
    scrollToElement(id) {
      let element_id = document.getElementById(id);
      if (element_id) {
        element_id.scrollIntoView({
          block: "center",
          behavior: "smooth"
        });
      }
    }
  },
};
</script>
<style lang="scss" scoped>
#logo {
    height: 50px;
}

.nav-item {
    cursor: pointer;
}
</style>

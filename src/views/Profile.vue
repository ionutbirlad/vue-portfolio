<template>
    <div class="profile-page">
        <section class="section-profile-cover section-shaped my-0">
            <div class="shape shape-style-1 shape-dark shape-skew alpha-4">
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <span></span>
            </div>
        </section>
        <section class="section section-skew">
            <div class="container">
                <card shadow class="card-profile mt--300" no-body>
                    <div class="px-4">
                        <div class="row justify-content-center">
                            <div class="col-lg-3 order-lg-2">
                                <div class="card-profile-image">
                                    <a href="#">
                                        <img v-lazy="'img/theme/me.jpeg'" class="rounded-circle">
                                    </a>
                                </div>
                            </div>
                            <div class="col-lg-4 order-lg-3 text-lg-right align-self-lg-center">
                                <div class="card-profile-actions py-4 mt-lg-0">
                                    <a target="_blank" rel="noopener noreferrer" href="https://www.linkedin.com/in/ionut-birlad-59a069151/">
                                      <base-button type="danger" size="sm" class="mr-4">
                                        <span><i class="fa fa-linkedin-square" aria-hidden="true"></i></span>
                                        LinkedIn
                                      </base-button>
                                    </a>
                                    <a target="_blank" rel="noopener noreferrer" href="https://github.com/ionutbirlad">
                                      <base-button type="default" size="sm" class="float-right">
                                        <span><i class="fa fa-github" aria-hidden="true"></i></span>
                                        GitHub
                                      </base-button>
                                    </a>
                                </div>
                            </div>

                            <div class="col-lg-4 order-lg-1">
                                <div class="card-profile-stats d-flex justify-content-center">
                                    <div>
                                        <span class="heading">22</span>
                                        <span class="description">Friends</span>
                                    </div>
                                    <div>
                                        <span class="heading">10</span>
                                        <span class="description">Photos</span>
                                    </div>
                                    <div>
                                        <span class="heading">89</span>
                                        <span class="description">Comments</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="text-center mt-5">
                            <h3>Ionut Birlad
                                <span class="font-weight-light">, 26</span>
                            </h3>
                            <div class="h6 font-weight-300"><i class="ni location_pin mr-2"></i>Trento, Trentino-Alto Adige, Italia</div>
                            <div class="h6 mt-4"><i class="ni business_briefcase-24 mr-2"></i>Full Stack Web Developer</div>
                            <!-- <div><i class="ni education_hat mr-2"></i>University of Computer Science</div> -->
                        </div>
                        <div class="mt-5 py-5 border-top text-center">
                            <div class="row justify-content-center">
                                <div class="col-lg-9">
                                  <p id="chisono">
                                    Sono un giovane Full Stack Web Developer con un background di formazione
                                    in ambito economico. Appassionato fin da giovanissimo di programmazione e informatica,
                                    oggi cerco di fondere le mie conoscenze e ottenere risultati implementando nuove
                                    tecnologie in un'ottica macroeconomica di mercato, studiando sempre nuovi strumenti
                                    da applicare e sviluppare.
                                  </p>
                                    <a href="#">Show more</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </card>
            </div>
        </section>

        <section class="section bg-secondary mb-5">
          <div class="container container-lg">
            <div class="row align-items-center justify-content-center">
              <h2 class="text-dark">Competenze</h2>
            </div>
            <tabs fill class="flex-column flex-md-row mt-4" id="competenze">
              <card shadow>
                  <tab-pane title="Frontend">
                    <span slot="title">
                        <i class="fa fa-television" aria-hidden="true"></i>
                        Frontend
                    </span>
                    <base-progress type="success" :value="100" label="HTML5" striped="true" animated="true"></base-progress>
                    <base-progress type="success" :value="98" label="CSS3" striped="true" animated="true"></base-progress>
                    <base-progress type="success" :value="95" label="Javascript" striped="true" animated="true"></base-progress>
                  </tab-pane>

                  <tab-pane title="Backend">
                    <span slot="title">
                        <i class="fa fa-terminal" aria-hidden="true"></i>
                        Backend
                    </span>
                    <base-progress type="success" :value="80" label="PHP" striped="true" animated="true"></base-progress>
                    <base-progress type="success" :value="85" label="MySQL" striped="true" animated="true"></base-progress>
                    <base-progress type="success" :value="90" label="MongoDB" striped="true" animated="true"></base-progress>
                    <base-progress type="success" :value="88" label="Node.js" striped="true" animated="true"></base-progress>
                  </tab-pane>

                  <tab-pane title="Frameworks e Librerie">
                    <span slot="title">
                        <i class="fa fa-cubes" aria-hidden="true"></i>
                        Frameworks e Librerie
                    </span>
                    <base-progress type="success" :value="88" label="Laravel" striped="true" animated="true"></base-progress>
                    <base-progress type="success" :value="90" label="Vue.js" striped="true" animated="true"></base-progress>
                    <base-progress type="success" :value="99" label="JQuery" striped="true" animated="true"></base-progress>
                    <base-progress type="success" :value="85" label="Bootstrap" striped="true" animated="true"></base-progress>
                    <base-progress type="success" :value="70" label="Wordpress" striped="true" animated="true"></base-progress>
                  </tab-pane>
              </card>
          </tabs>
          </div>
        </section>

        <section class="section section-lg section-shaped overflow-hidden my-0" id="progetti">
          <div class="shape shape-style-1 shape-dark shape-skew alpha-4">
              <span></span>
              <span></span>
              <span></span>
              <span></span>
              <span></span>
              <span></span>
              <span></span>
          </div>
          <div class="container container-lg">
            <div class="row align-items-center justify-content-center">
              <h2 class="text-white">Progetti principali</h2>
            </div>

            <!-- modal progetti -->
            <modal :show.sync="modal">
              <h6 slot="header" class="modal-title" id="modal-title-default"> {{openedProject.title}} <small class="text-muted"> {{openedProject.subtitle}} </small> </h6>

              {{openedProject.description}}

              <template slot="footer">
                  <!-- <base-button type="primary">Esplora altri progetti</base-button> -->
                  <base-button type="link" class="ml-auto" @click="modal = false">Chiudi
                  </base-button>
              </template>
            </modal>

              <div class="row">
                  <div @click="(modal = true) && (openedProject = projects.boolflix)" class="col col-sm-6 mb-5 mt-4 mb-md-5 pt-3 slide-in from-left" v-b-popover.hover.top="'Clicca sul progetto per maggiori informazioni'"
           :title="projects.boolflix.subtitle">
                      <div class="card card-lift--hover shadow border-0">
                        <img v-lazy="projects.boolflix.image" class="card-img">
                      </div>
                  </div>
                  <div @click="(modal = true) && (openedProject = projects.spotify)" class="col col-sm-6 mb-5 mt-4 mb-md-5 pt-3 slide-in from-right" v-b-popover.hover.top="'Clicca sul progetto per maggiori informazioni'"
           :title="projects.spotify.subtitle">
                      <div class="card card-lift--hover shadow border-0">
                        <img v-lazy="projects.spotify.image" class="card-img">
                      </div>
                  </div>
              </div>
              <div class="row">
                  <div @click="(modal = true) && (openedProject = projects.airbnb)" class="col-6 col-md-4 mb-5 mt-4 mb-md-5 pt-3 fade-in" v-b-popover.hover.topleft="'Clicca sul progetto per maggiori informazioni'"
           :title="projects.airbnb.subtitle">
                      <div class="card card-lift--hover shadow border-0">
                        <img v-lazy="projects.airbnb.image" class="card-img">
                      </div>
                  </div>
                  <div @click="(modal = true) && (openedProject = projects.whatsapp)" class="col-6 col-md-4 mb-5 mt-4 mb-md-5 pt-3 fade-in" v-b-popover.hover.topright="'Clicca sul progetto per maggiori informazioni'"
           :title="projects.whatsapp.subtitle">
                      <div class="card card-lift--hover shadow border-0">
                        <img v-lazy="projects.whatsapp.image" class="card-img">
                      </div>
                  </div>
                  <div @click="(modal = true) && (openedProject = projects.teambit)" class="col-6 col-md-4 mb-5 mt-4 mb-md-5 pt-3 fade-in" v-b-popover.hover.top="'Clicca sul progetto per maggiori informazioni'"
           :title="projects.teambit.subtitle">
                      <div class="card card-lift--hover shadow border-0">
                        <img v-lazy="projects.teambit.image" class="card-img">
                      </div>
                  </div>
              </div>
          </div>
        </section>

        <section class="section section-lg section-shaped overflow-hidden my-0 pb-0">
          <div class="container container-lg">
            <div class="row align-items-center justify-content-center pb-3">
              <h2 class="text-dark">Formazione</h2>
            </div>
            <div class="row" id="formazione">
              <!-- <div class="col-md-6 col-sm-6 mb-5 mt-4 mb-md-5 pt-3"> -->
                <div class="transform-perspective-left col-md-6 col-sm-6 mb-5 mt-4 mb-md-5">
                  <div class="card card-lift--hover shadow border-0 slide-in from-left">
                      <router-link to="/landing" title="Landing Page">
                          <img v-lazy="'img/theme/landing.jpg'" class="card-img">
                      </router-link>
                  </div>
                </div>
              <!-- </div> -->
              <!-- <div class="col-md-6 col-sm-6 mb-5 mt-4 mb-md-5 pt-3"> -->
                <div class="transform-perspective-right col-md-6 col-sm-6 mb-5 mt-4 mb-md-5">
                  <div class="card card-lift--hover shadow border-0 slide-in from-right">
                      <router-link to="/landing" title="Landing Page">
                          <img v-lazy="'img/theme/landing.jpg'" class="card-img">
                      </router-link>
                  </div>
                </div>
              <!-- </div> -->
            </div>

            <div class="row">
              <!-- <div class="col-md-6 col-sm-6 mb-5 mt-4 mb-md-5 pt-3"> -->
                <div class="transform-perspective-left col-md-6 col-sm-6 mb-5 mt-4 mb-md-5">
                  <div class="card card-lift--hover shadow border-0 slide-in from-left">
                      <router-link to="/landing" title="Landing Page">
                          <img v-lazy="'img/theme/landing.jpg'" class="card-img">
                      </router-link>
                  </div>
                </div>
              <!-- </div> -->
              <!-- <div class="col-md-6 col-sm-6 mb-5 mt-4 mb-md-5 pt-3"> -->
                <div class="transform-perspective-right col-md-6 col-sm-6 mb-5 mt-4 mb-md-5">
                  <div class="card card-lift--hover shadow border-0 slide-in from-right">
                      <router-link to="/landing" title="Landing Page">
                          <img v-lazy="'img/theme/landing.jpg'" class="card-img">
                      </router-link>
                  </div>
                </div>
              <!-- </div> -->
            </div>
          </div>
        </section>
    </div>
</template>

<script scoped>
import Tabs from "@/components/Tabs/Tabs.vue";
import TabPane from "@/components/Tabs/TabPane.vue";
import { VBTooltip } from "bootstrap-vue/esm/directives/tooltip/tooltip";
import { VBPopover } from "bootstrap-vue/esm/directives/popover/popover";
import Modal from "@/components/Modal.vue";

export default {
  directives: {
    BTooltip: VBTooltip,
    BPopover: VBPopover,
  },
  components: {
    'tabs': Tabs,
    'tab-pane': TabPane,
    Modal
  },
  data () {
    return {
      modal: false,
      openedProject: '',
      projects: {
        boolflix: { title: 'Boolflix', subtitle: 'Progetto ispirato a Netflix', description: "Progetto ispirato al famoso Netflix, costruito utilizzando esclusivamente HTML5, CSS3 e Javascript, insieme ad alcune librerie e framework (JQuery per la parte dinamica di User Interface e Owl Carousel per ottenere lo slider con l'insieme dei film/serie TV ricercati in ogni sezione). Per quanto riguarda la ricerca dei contenuti multimediali ho utilizzato le API personalizzate messe a disposizione da 'TMDB', interrogate dalle chiamate AJAX di JQuery. I risultati inoltre sono filtrabili per 'film' o per 'serie tv'.", image: "img/projects_cover/boolflix.png"},

        spotify: { title: 'Spotify', subtitle: 'Progetto ispirato a Spotify', description: "Interfaccia grafica per player musicale ispirato a Spotify Web, il colosso dei servizi di musica. Qui ho utilizzato procedure avanzate di CSS3 per ottenere vari effetti visivi, come ad esempio le cards 3D. Template completamente resposive e orientato al 'mobile first'", image: "img/projects_cover/spotify.png"},

        airbnb: { title: 'BoolBnB', subtitle: 'Progetto ispirato ad AirBnB', description: "Progetto realizzato partendo da zero e lavorando in team. Una complessa Applicazione Web ispirata al famoso Airbnb, completa di Backend (autenticazione in base a Ruoli, gestione di un Payment Provider, Geolocalizzazione API, Cron Job per la gestione delle sponsorizzazioni e completa di tutte le operazioni CRUD per quanto riguarda la gestione degli appartamenti) e interfaccia Frontend responsive. Quest'ultima è stata generata con Blade Template Engine.", image: "img/projects_cover/airbnb.png"},

        whatsapp: { title: 'BoolsApp', subtitle: 'Progetto ispirato a WhatsApp Web', description: "Interfaccia full responsive che simula il funzionamento e la gestione dei messaggi di WhatsApp Web. Insieme ad HTML5, CSS3 e Javascript ho utilizzato Jquery come framework per la gestione delle varie interazioni grafiche ed Handlebars.js come template engine per la generazione dei messaggi. Inoltre l'app consente la gestione e l'aggiunta dei propri contatti e la ricerca all'interno degli stessi.", image: "img/projects_cover/boolsapp.png"},

        teambit: { title: 'Teambit', subtitle: 'Progetto ispirato a Teambit', description: "Template del sito web di Teambit, riprodotto nei minimi dettagli usando esclusivamente custom CSS. Oltre ad HTML5, CSS3 e Javascript ho utilizzzato in fase di developing Webpack per la gestione della compilazione dei file SCSS e JS. Interamente responsive.", image: "img/projects_cover/teambit.png"},
      },
    }
  },
  mounted () {
    // faders effect
    const faders = document.querySelectorAll(".fade-in");

    const appearOptions = {
      threshold: 0,
      rootMargin: "0px 0px -250px 0px"
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

    // slide in effect
    const sliders = document.querySelectorAll(".slide-in");

    sliders.forEach(slider => {
      appearOnScroll.observe(slider);
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

// slide in
.from-left {
  // grid-column: 2 / 3;
  -webkit-transform: translateX(-50%);
  transform: translateX(-50%);
}

.from-right {
  // grid-column: 3 / 4;
  -webkit-transform: translateX(50%);
  transform: translateX(50%);
}

.from-left,
.from-right {
  transition: opacity 250ms ease-in, -webkit-transform 400ms ease-in;
  transition: opacity 250ms ease-in, transform 400ms ease-in;
  transition: opacity 250ms ease-in, transform 400ms ease-in,
    -webkit-transform 400ms ease-in;
  opacity: 0;
  &.appear {
    -webkit-transform: translateX(0);
    transform: translateX(0);
    opacity: 1;
  }
}

.card {
  cursor: pointer;
}

#progetti {
  height: 794.16px;
  padding-bottom: 0;
}

</style>

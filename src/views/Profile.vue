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
                <div class="mr-0">
                  <span class="heading"><i class="fa fa-cutlery" aria-hidden="true"></i></span>
                  <span class="description">eat();</span>
                </div>
                <div class="mr-0">
                  <span class="heading"><i class="fa fa-bed" aria-hidden="true"></i></span>
                  <span class="description">sleep();</span>
                </div>
                <div class="mr-0">
                  <span class="heading"><i class="fa fa-code" aria-hidden="true"></i></span>
                  <span class="description">code();</span>
                </div>
                <div class="mr-0">
                  <span class="heading"><i class="fa fa-repeat" aria-hidden="true"></i></span>
                  <span class="description">repeat();</span>
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
        <h2 class="display-3">Competenze</h2>
      </div>
      <tabs fill class="flex-column flex-md-row mt-4" id="competenze">
        <card shadow>
          <tab-pane class="increment" title="Frontend">
            <span slot="title">
              <i class="fa fa-television" aria-hidden="true"></i>
              Frontend
            </span>
            <base-progress type="success" :value="competenze.html.value" label="HTML5" striped="true" animated="true"></base-progress>
            <base-progress type="success" :value="competenze.css.value" label="CSS3" striped="true" animated="true"></base-progress>
            <base-progress type="success" :value="competenze.javascript.value" label="Javascript" striped="true" animated="true"></base-progress>
          </tab-pane>

          <tab-pane class="increment" title="Backend">
            <span slot="title">
              <i class="fa fa-terminal" aria-hidden="true"></i>
              Backend
            </span>
            <base-progress type="success" :value="competenze.php.value" label="PHP" striped="true" animated="true"></base-progress>
            <base-progress type="success" :value="competenze.mysql.value" label="MySQL" striped="true" animated="true"></base-progress>
            <base-progress type="success" :value="competenze.mongodb.value" label="MongoDB" striped="true" animated="true"></base-progress>
            <base-progress type="success" :value="competenze.nodejs.value" label="Node.js" striped="true" animated="true"></base-progress>
          </tab-pane>

          <tab-pane class="increment" title="Frameworks e Librerie">
            <span slot="title">
              <i class="fa fa-cubes" aria-hidden="true"></i>
              Frameworks e Librerie
            </span>
            <base-progress type="success" :value="competenze.laravel.value" label="Laravel" striped="true" animated="true"></base-progress>
            <base-progress type="success" :value="competenze.vuejs.value" label="Vue.js" striped="true" animated="true"></base-progress>
            <base-progress type="success" :value="competenze.jquery.value" label="JQuery" striped="true" animated="true"></base-progress>
            <base-progress type="success" :value="competenze.bootstrap.value" label="Bootstrap" striped="true" animated="true"></base-progress>
            <base-progress type="success" :value="competenze.wordpress.value" label="Wordpress" striped="true" animated="true"></base-progress>
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
        <h2 class="display-3 text-white">Progetti principali</h2>
      </div>

      <!-- modal progetti -->
      <modal :show.sync="modalProgetti">
        <h6 slot="header" class="modal-title" id="modal-title-default"> {{openedProject.title}} <small class="text-muted"> {{openedProject.subtitle}} </small> </h6>

        <p>{{openedProject.description}}</p>

        <small>Al seguente link è possibile vedere il codice sorgente del progetto: <a :href="openedProject.link">{{openedProject.link}}</a> </small>

        <template slot="footer">
          <base-button type="link" class="ml-auto" @click="modalProgetti = false">Chiudi
          </base-button>
        </template>
      </modal>

      <div class="row">
        <div @click="(modalProgetti = true) && (openedProject = projects.boolflix)" class="col col-sm-6 mb-5 mt-4 mb-md-5 pt-3 slide-in from-left" v-b-popover.hover.top :title="popMessage">
          <div class="card card-lift--hover shadow border-0">
            <img v-lazy="projects.boolflix.image" class="card-img">
          </div>
        </div>
        <div @click="(modalProgetti = true) && (openedProject = projects.spotify)" class="col col-sm-6 mb-5 mt-4 mb-md-5 pt-3 slide-in from-right" v-b-popover.hover.top :title="popMessage">
          <div class="card card-lift--hover shadow border-0">
            <img v-lazy="projects.spotify.image" class="card-img">
          </div>
        </div>
      </div>
      <div class="row">
        <div @click="(modalProgetti = true) && (openedProject = projects.airbnb)" class="col-6 col-md-4 mb-5 mt-4 mb-md-5 pt-3 fade-in" v-b-popover.hover.topleft :title="popMessage">
          <div class="card card-lift--hover shadow border-0">
            <img v-lazy="projects.airbnb.image" class="card-img">
          </div>
        </div>
        <div @click="(modalProgetti = true) && (openedProject = projects.whatsapp)" class="col-6 col-md-4 mb-5 mt-4 mb-md-5 pt-3 fade-in" v-b-popover.hover.topright :title="popMessage">
          <div class="card card-lift--hover shadow border-0">
            <img v-lazy="projects.whatsapp.image" class="card-img">
          </div>
        </div>
        <div @click="(modalProgetti = true) && (openedProject = projects.teambit)" class="col-6 col-md-4 mb-5 mt-4 mb-md-5 pt-3 fade-in" v-b-popover.hover.top :title="popMessage">
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
        <h2 class="display-3">Formazione</h2>
      </div>
      <div class="row" id="formazione">
        <div class="transform-perspective-left col-md-6 col-sm-6 mb-5 mt-4 mb-md-5">
          <div class="card-wrapper-left slide-in from-left">
            <card class="card border-0" shadow body-classes="py-5">
              <img v-lazy="'img/brand/boolean.png'" alt="Raised circle image" class="img-fluid rounded-circle shadow-lg mb-4" style="width: 80px;">
              <h6 class="text-primary text-uppercase">Boolean Careers</h6>
              <div class="description mt-3">
                <p class="my-0">Corso intensivo Full Stack Web Developer a tempo pieno, con forte attività pratica sia individuale che in team.</p>
                <div class="row noOnMobile">
                  <p class="mb-1 ml-3">In particolare abbiamo utilizzato le seguenti tecnologie:</p>
                  <div class="col-md-6">
                    <ul class="my-0">
                      <li>HTML</li>
                      <li>CSS</li>
                      <li>Javascript ES5 / ES6</li>
                      <li>PHP (OOP)</li>
                      <li>Node.Js</li>
                    </ul>
                    <p class="mb-0">Framework Back-end:</p>
                    <ul class="my-0">
                      <li>Laravel</li>
                    </ul>
                    <p class="mb-0">Database:</p>
                    <ul class="my-0">
                      <li>MySql</li>
                    </ul>
                    <p class="mb-0">Framework Front-end:</p>
                    <ul class="my-0">
                      <li>JQuery</li>
                      <li>VueJs</li>
                    </ul>
                  </div>
                  <div class="col-md-6">
                    <p class="mb-0">CSS:</p>
                    <ul class="my-0">
                      <li>Puro</li>
                      <li>SASS / SCSS</li>
                      <li>Bootstrap 3 e 4</li>
                    </ul>
                    <p class="mb-0">Tools:</p>
                    <ul class="my-0">
                      <li>Webpack</li>
                      <li>Chart.Js</li>
                      <li>HandleBars</li>
                    </ul>
                    <p class="mb-0">Versioning Tool:</p>
                    <ul class="my-0">
                      <li>Git</li>
                    </ul>
                  </div>
                </div>
              </div>
              <div class="mt-3">
                <badge type="primary" rounded>programmazione</badge>
                <badge type="primary" rounded>sviluppo web</badge>
                <badge type="primary" rounded>frontend</badge>
                <badge type="primary" rounded>backend</badge>
              </div>
              <base-button tag="a" href="https://www.boolean.careers/" target="_blank" rel="noopener noreferrer" type="primary" class="mt-4">
                Scopri di più
              </base-button>
            </card>
          </div>
        </div>
        <div class="transform-perspective-right col-md-6 col-sm-6 mb-5 mt-4 mb-md-5">
          <div class="card-wrapper-right slide-in from-right">
            <card class="card border-0" shadow body-classes="py-5">
              <img v-lazy="'img/brand/unisi.jpg'" alt="Raised circle image" class="img-fluid rounded-circle shadow-lg mb-4" style="width: 80px;">
              <h6 class="text-primary text-uppercase">Università degli Studi di Siena</h6>
              <div class="description mt-3">
                <p class="siena">Laurea triennale in Scienze dell'Economia e della Gestione Aziendale.</p>
                <div class="resizeIntermedio"></div>
                <div class="row noOnMobile">
                  <p class="ml-3 siena">Percorso formativo che approfondisce le
                  seguenti 4 aree disciplinari:</p>
                  <div class="col-6 px-0">
                    <ul>
                      <li class="mb-3">aziendale (le tecniche di rilevazione dei fenomeni aziendali e
                        della loro traduzione in scritture contabili, l'analisi strategica
                        dell'impresa, il marketing)</li>
                      <li class="mb-3">economica (microeconomia, tratta l'analisi del consumatore e dell'impresa,
                        e macroeconomia,
                        riguardo l'equilibrio macroeconomico e l'economia pubblica)</li>
                    </ul>
                  </div>
                  <div class="col-6 px-0">
                    <ul>
                      <li class="mb-3">giuridica (diritto pubblico, diritto privato, diritto commerciale e diritto tributario)</li>
                      <li class="mb-3">matematico-statistica (matematica generale, matematica finanziaria e statistica
                        applicati alla realtà economico aziendale)</li>
                    </ul>
                  </div>
                </div>
              </div>
              <div>
                <badge type="primary" rounded>economia</badge>
                <badge type="primary" rounded>marketing</badge>
                <badge type="primary" rounded>informatica</badge>
              </div>
              <base-button tag="a" href="https://www.unisi.it/ugov/degree/9744" target="_blank" rel="noopener noreferrer" type="primary" class="mt-4">
                Scopri di più
              </base-button>
            </card>
          </div>
        </div>
      </div>

      <div class="row">
        <div class="transform-perspective-left col-md-6 col-sm-6 mb-5 mt-4 mb-md-5">
          <div class="card-wrapper-left slide-in from-left">
            <card class="card border-0" shadow body-classes="py-5">
              <img v-lazy="'img/brand/bandini.png'" alt="Raised circle image" class="img-fluid rounded-circle shadow-lg mb-4 py-2 px-2" style="width: 80px;">
              <h6 class="text-primary text-uppercase">Istituto Tecnico Commerciale "Sallustio Bandini" - Siena (Ragioneria)</h6>
              <p class="description mt-3">Diploma Tecnico Commerciale - Indirizzo Sistemi informativi aziendali <br>
                Percorso di specializzazione che affianca
                allo studio dell’amministrazione e della
                gestione dell’azienda.</p>
                <div class="resizeIntermedio"></div>
              <div>
                <badge type="primary" rounded>economia</badge>
                <badge type="primary" rounded>informatica</badge>
              </div>
              <base-button tag="a" href="https://www.istitutobandini.it/newSite/sistemi-informativi-aziendali-triennio" target="_blank" rel="noopener noreferrer" type="primary" class="mt-4">
                Scopri di più
              </base-button>
            </card>
          </div>
        </div>
        <div class="transform-perspective-right col-md-6 col-sm-6 mb-5 mt-4 mb-md-5">
          <div class="card-wrapper-right slide-in from-right">
            <card class="card border-0" shadow body-classes="py-5">
              <img v-lazy="'img/brand/google.png'" alt="Raised circle image" class="img-fluid rounded-circle shadow-lg mb-4 py-2 px-2" style="width: 80px;">
              <h6 class="text-primary text-uppercase">Google Digital Trainning - Fondamenti di Marketing Digitale</h6>
              <p class="description mt-3">Corso creato da formatori Google e accreditato dall'Interactive Advertising Bureau,
                che tratta aspetti fondamentali del marketing digitale e analizza casi studio reali per aiutare a mettere in pratica le conoscenze acquisite.</p>
              <div>
                <badge type="primary" rounded>SEM</badge>
                <badge type="primary" rounded>SEO</badge>
                <badge type="primary" rounded>google analytics</badge>
                <badge type="primary" rounded>analisi dati</badge>
                <badge type="primary" rounded>marketing digitale</badge>
              </div>
              <base-button tag="a" href="https://learndigital.withgoogle.com/digitaltraining/courses" target="_blank" rel="noopener noreferrer" type="primary" class="mt-4">
                Scopri di più
              </base-button>
            </card>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="certificazioni" class="section section-lg section-nucleo-icons pt-100 pb-0">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-8 text-center">
          <h2 class="display-3">Licenze e Certificazioni</h2>
          <h4 class="text-muted mb-5">Clicca sul pulsante per vederle tutte!</h4>
          <div class="btn-wrapper">
            <base-button @click="showIconsAnimation = !showIconsAnimation" type="primary">Mostra</base-button>
          </div>
        </div>
        <!-- modal certificazioni -->
        <modal :show.sync="modalCertificazioni">
          <h6 slot="header" class="modal-title" id="modal-title-default"> {{openedCertification.title}} </h6>

          <small class="text-muted">Oraganizzazione emittente: </small> {{openedCertification.organizzazioneEmittente}} <br>
          <small class="text-muted">Data rilascio: </small> {{openedCertification.dataRilascio}} <br>
          <small class="text-muted">ID Credenziale: </small> {{openedCertification.idCredenziale}} <br>
          <small v-if="openedCertification.urlCredenziale" class="text-muted">Url Credenziale:
          </small>
          <a :href="openedCertification.urlCredenziale" target="_blank" rel="noopener noreferrer"> <small>{{openedCertification.urlCredenziale}}
            </small>
          </a>

          <template slot="footer">
            <base-button type="link" class="ml-auto" @click="modalCertificazioni = false">Chiudi
            </base-button>
          </template>
        </modal>
      </div>
      <div class="section-nucleo-icons icons-container blur-item mt-0" :class="{'on-screen': showIconsAnimation}">
        <!-- Center -->
        <i class="icon ni ni-diamond"></i>
        <!-- Right 1 -->
        <span></span>
        <i @click="(modalCertificazioni = true) && (openedCertification = certificazioni.delf)" class="icon icon-sm fa fa-language" aria-hidden="true" v-b-popover.hover.top :title="popMessage"></i>
        <i @click="(modalCertificazioni = true) && (openedCertification = certificazioni.googleTraining)" class="icon icon-sm fa fa-google" aria-hidden="true" v-b-popover.hover.top :title="popMessage"></i>
        <!-- Right 2 -->
        <span></span>
        <span></span>
        <span></span>
        <!-- Left 1 -->
        <span></span>
        <i @click="(modalCertificazioni = true) && (openedCertification = certificazioni.cambridge)" class="icon icon-sm fa fa-language" aria-hidden="true" v-b-popover.hover.top :title="popMessage"></i>
        <i @click="(modalCertificazioni = true) && (openedCertification = certificazioni.booleanCareers)" class="icon icon-sm fa fa-certificate" aria-hidden="true" v-b-popover.hover.top :title="popMessage"></i>

        <!-- Left 2 -->
        <span></span>
        <span></span>
        <span></span>

      </div>
    </div>
  </section>

</div>
</template>

<script scoped>
import Tabs from "@/components/Tabs/Tabs.vue";
import TabPane from "@/components/Tabs/TabPane.vue";
import {
  VBTooltip
} from "bootstrap-vue/esm/directives/tooltip/tooltip";
import {
  VBPopover
} from "bootstrap-vue/esm/directives/popover/popover";
import Modal from "@/components/Modal.vue";
import Icons from "./components/Icons";

export default {
  directives: {
    BTooltip: VBTooltip,
    BPopover: VBPopover,
  },
  components: {
    'tabs': Tabs,
    'tab-pane': TabPane,
    Modal,
    Icons
  },
  data() {
    return {
      windowWidth: window.innerWidth,
      popMessage: '',
      modalProgetti: false,
      modalCertificazioni: false,
      showIconsAnimation: false,
      competenze: {
        html: {
          value: 0,
          increment: 100
        },
        css: {
          value: 0,
          increment: 98
        },
        javascript: {
          value: 0,
          increment: 95
        },
        php: {
          value: 0,
          increment: 80
        },
        mysql: {
          value: 0,
          increment: 85
        },
        mongodb: {
          value: 0,
          increment: 90
        },
        nodejs: {
          value: 0,
          increment: 88
        },
        laravel: {
          value: 0,
          increment: 88
        },
        vuejs: {
          value: 0,
          increment: 90
        },
        jquery: {
          value: 0,
          increment: 99
        },
        bootstrap: {
          value: 0,
          increment: 85
        },
        wordpress: {
          value: 0,
          increment: 70
        }
      },
      openedProject: '',
      projects: {
        boolflix: {
          title: 'Boolflix',
          subtitle: 'Progetto ispirato a Netflix',
          description: "Progetto ispirato al famoso Netflix, costruito utilizzando esclusivamente HTML5, CSS3 e Javascript, insieme ad alcune librerie e framework (JQuery per la parte dinamica di User Interface e Owl Carousel per ottenere lo slider con l'insieme dei film/serie TV ricercati in ogni sezione). Per quanto riguarda la ricerca dei contenuti multimediali ho utilizzato le API personalizzate messe a disposizione da 'TMDB', interrogate dalle chiamate AJAX di JQuery. I risultati inoltre sono filtrabili per 'film' o per 'serie tv'.",
          image: "img/projects_cover/boolflix.png",
          link: 'https://github.com/ionutbirlad/ajax-ex-boolflix'
        },

        spotify: {
          title: 'Spotify',
          subtitle: 'Progetto ispirato a Spotify',
          description: "Interfaccia grafica per player musicale ispirato a Spotify Web, il colosso dei servizi di musica. Qui ho utilizzato procedure avanzate di CSS3 per ottenere vari effetti visivi, come ad esempio le cards 3D. Template completamente resposive e orientato al 'mobile first'",
          image: "img/projects_cover/spotify.png",
          link: 'https://github.com/ionutbirlad/html-css-spotifyweb'
        },

        airbnb: {
          title: 'BoolBnB',
          subtitle: 'Progetto ispirato ad AirBnB',
          description: "Progetto realizzato partendo da zero e lavorando in team. Una complessa Applicazione Web ispirata al famoso Airbnb, completa di Backend (autenticazione in base a Ruoli, gestione di un Payment Provider, Geolocalizzazione API, Cron Job per la gestione delle sponsorizzazioni e completa di tutte le operazioni CRUD per quanto riguarda la gestione degli appartamenti) e interfaccia Frontend responsive. Quest'ultima è stata generata con Blade Template Engine.",
          image: "img/projects_cover/airbnb.png",
          link: 'https://github.com/ionutbirlad/laravel-BoolBnB'
        },

        whatsapp: {
          title: 'BoolsApp',
          subtitle: 'Progetto ispirato a WhatsApp Web',
          description: "Interfaccia full responsive che simula il funzionamento e la gestione dei messaggi di WhatsApp Web. Insieme ad HTML5, CSS3 e Javascript ho utilizzato Jquery come framework per la gestione delle varie interazioni grafiche ed Handlebars.js come template engine per la generazione dei messaggi. Inoltre l'app consente la gestione e l'aggiunta dei propri contatti e la ricerca all'interno degli stessi.",
          image: "img/projects_cover/boolsapp.png",
          link: 'https://github.com/ionutbirlad/js-html-css-boolzap'
        },

        teambit: {
          title: 'Teambit',
          subtitle: 'Progetto ispirato a Teambit',
          description: "Template del sito web di Teambit, riprodotto nei minimi dettagli usando esclusivamente custom CSS. Oltre ad HTML5, CSS3 e Javascript ho utilizzzato in fase di developing Webpack per la gestione della compilazione dei file SCSS e JS. Interamente responsive.",
          image: "img/projects_cover/teambit.png",
          link: 'https://github.com/ionutbirlad/node-sass-teambit'
        },
      },
      openedCertification: '',
      certificazioni: {
        booleanCareers: {
          title: 'Corso FullStack Web Developer FullTime',
          organizzazioneEmittente: 'Boolean Careers',
          dataRilascio: 'Giugno 2020',
          idCredenziale: '20071656',
          urlCredenziale: 'https://www.credential.net/ba29f733-ef40-4c40-8f01-eb4764bfc9de#gs.95m6tt',
          image: "img/projects_cover/boolflix.png"
        },
        googleTraining: {
          title: 'Google Digital Trainning - Fondamenti di Marketing Digitale',
          organizzazioneEmittente: 'Google',
          dataRilascio: 'Agosto 2019',
          idCredenziale: '3RA 9QQ P95'
        },
        cambridge: {
          title: 'Certificato Cambridge Lingua Inglese',
          organizzazioneEmittente: 'Cambridge Assessment International Education',
          dataRilascio: 'Aprile 2014',
          idCredenziale: '0043993694'
        },
        delf: {
          title: 'Diploma di studio lingua francese',
          organizzazioneEmittente: "Ministère de l'Éducation nationale et de la Jeunesse",
          dataRilascio: 'Novembre 2009',
          idCredenziale: '039055-016642'
        },
      },
    }
  },
  mounted() {
    let that = this;
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

    // increment effect
    const tabPanes = document.querySelectorAll(".increment");

    const incrementOnScroll = new IntersectionObserver(function(
        entries,
        incrementOnScroll
      ) {
        entries.forEach(entry => {
          if (!entry.isIntersecting) {
            return;
          } else {
            for (var competenza in that.competenze) {
              that.competenze[competenza].value = that.competenze[competenza].increment;
            }
            incrementOnScroll.unobserve(entry.target);
          }
        });
      },
      appearOptions);

    tabPanes.forEach(fader => {
      incrementOnScroll.observe(fader);
    });

    // gestione tooltip on resize
    window.onresize = () => {
      that.windowWidth = window.innerWidth
      that.windowWidth <= 768 ? that.popMessage = '' : that.popMessage = 'Clicca per maggiori informazioni'
    }
    that.windowWidth <= 768 ? that.popMessage = '' : that.popMessage = 'Clicca per maggiori informazioni'
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
  -webkit-transform: translateX(-50%);
  transform: translateX(-50%);
}

.from-right {
  -webkit-transform: translateX(50%);
  transform: translateX(50%);
}

.from-left,
.from-right {
  transition: opacity 250ms ease-in, -webkit-transform 400ms ease-in;
  transition: opacity 250ms ease-in, transform 400ms ease-in;
  transition: opacity 250ms ease-in, transform 400ms ease-in, -webkit-transform 400ms ease-in;
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

.card-wrapper-left {
  position: relative;
  & > .card {
    border: 1px solid #00000080 !important;
  }
  &::before {
    content: "";
    width: 100%;
    height: 100%;
    position: absolute;
    z-index: -39999999;
    background: rgb(50,50,93);
    background: linear-gradient(120deg, rgba(50,50,93,1) 47%, rgba(192,57,43,1) 100%);
    transform: translate(-2%, -2%);
    border-radius: 5px;
  }
}

.card-wrapper-right {
  position: relative;
  & > .card {
    border: 1px solid #00000080 !important;
  }
  &::before {
    content: "";
    width: 100%;
    height: 100%;
    position: absolute;
    z-index: -39999999;
    background: rgb(50,50,93);
    background: linear-gradient(120deg, rgba(50,50,93,1) 47%, rgba(192,57,43,1) 100%);
    transform: translate(2%, -2%);
    border-radius: 5px;
  }
}

.icon {
  cursor: pointer;
}

// .resizeIntermedio {
//   height: 38px;
// }

@media screen and (max-width: 991px) {
  .noOnMobile {
    display: none;
  }
}

@media screen and (min-width: 576px) and (max-width: 991px) {
  .resizeIntermedio {
    height: 49px;
  }
}

@media screen and (min-width: 991px) and (max-width: 1150px) {
  p.siena {
    font-size: 0.9rem;
  }
}
</style>

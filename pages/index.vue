<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="12">
      <!-- <v-card class="logo py-4 d-flex justify-center">
        <NuxtLogo />
        <VuetifyLogo />
      </v-card> -->
      <v-card>
        <v-img
          :src="require('~/assets/images/clearhome.jpg')"
          class="dark--text align-center imagehome"
          gradient="to top left, rgba(50,50,50,.11), rgba(25,32,72,.5)"
          dark
        >
          <div class="fill-height bottom-gradient"></div>
          <v-row justify="center" align="center">
            <v-col cols="12" md="6">
              <v-card-title class="text-h4">Pre-fab homes</v-card-title>
              <v-card-subtitle class="text-h6">
                Curb Appeal Power Clean es una empresa de lavado a presión que se dedica a
                brindar servicios de alta calidad y completa satisfacción a sus clientes
                en todo el condado de Los Ángeles. ¡Llámenos hoy para una cotización
                gratis
              </v-card-subtitle>
            </v-col>
            <v-col cols="12" md="4">
              <form-home></form-home>
            </v-col>
          </v-row>
        </v-img>
      </v-card>

      <!-- <v-row dense>
        <v-col cols="12">
          <v-card color="#385F73" dark>
            <v-card-title class="text-h5"> Unlimited music now </v-card-title>

            <v-card-subtitle
              >Listen to your favorite artists and albums whenever and wherever, online
              and offline.</v-card-subtitle
            >

            <v-card-actions>
              <v-btn text> Listen Now </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row> -->
      <v-card>
        <v-card-title class="headline d-flex justify-center">
          Welcome to the Vuetify + Nuxt.js template
        </v-card-title>
        <v-card-text>
          <p>
            Vuetify is a progressive Material Design component framework for Vue.js. It
            was designed to empower developers to create amazing applications.
          </p>
          <p>
            For more information on Vuetify, check out the
            <a href="https://vuetifyjs.com" target="_blank" rel="noopener noreferrer">
              documentation </a
            >.
          </p>
          <p>
            If you have questions, please join the official
            <a
              href="https://chat.vuetifyjs.com/"
              target="_blank"
              rel="noopener noreferrer"
              title="chat"
            >
              discord </a
            >.
          </p>
          <p>
            Find a bug? Report it on the github
            <a
              href="https://github.com/vuetifyjs/vuetify/issues"
              target="_blank"
              rel="noopener noreferrer"
              title="contribute"
            >
              issue board </a
            >.
          </p>
          <p>
            Thank you for developing with Vuetify and I look forward to bringing more
            exciting features in the future.
          </p>
          <div class="text-xs-right">
            <em><small>&mdash; John Leider</small></em>
          </div>
          <hr class="my-3" />
          <a href="https://nuxtjs.org/" target="_blank" rel="noopener noreferrer">
            Nuxt Documentation
          </a>
          <br />
          <a
            href="https://github.com/nuxt/nuxt.js"
            target="_blank"
            rel="noopener noreferrer"
          >
            Nuxt GitHub
          </a>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn color="primary" nuxt to="/inspire"> Continue </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
import FormHome from "../components/home/FormHome.vue";
export default {
  components: { FormHome },
  name: "IndexPage",
};
</script>
<style>
.imagehome {
  color: top left, rgba(50, 50, 50, 0.1), rgba(12, 29, 126, 0.5);
}
</style>

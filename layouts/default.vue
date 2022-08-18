<template>
  <v-app>
    <v-card class="d-flex">
      <v-app-bar fixed app>
        <v-toolbar-title class="text-h6 text-sm-h4"
          ><v-avatar :tile="true">
            <img :src="require('@/static/vuetify-logo.svg')" alt="logo" /> </v-avatar
          >Page titlesfasaf</v-toolbar-title
        >

        <template v-slot:extension>
          <v-tabs v-model="currentItem" centered>
            <v-menu bottom left open-on-hover>
              <template v-slot:activator="{ on, attrs }">
                <v-btn text class="align-self-center mr-4" v-bind="attrs" v-on="on">
                  Services
                  <v-icon right> mdi-menu-down </v-icon>
                </v-btn>
              </template>

              <v-list class="grey lighten-3">
                <v-list-item
                  v-for="item in services"
                  :key="item"
                  :to="'/services/' + item"
                >
                  {{ item }}
                </v-list-item>
              </v-list>
            </v-menu>

            <v-tab v-for="item in itemsTab" :key="item" :to="'/' + item">
              {{ item }}
            </v-tab>

            <!-- <v-menu bottom left>
              <template v-slot:activator="{ on, attrs }">
                <v-btn text class="align-self-center mr-4" v-bind="attrs" v-on="on">
                  more
                  <v-icon right> mdi-menu-down </v-icon>
                </v-btn>
              </template>

              <v-list class="grey lighten-3">
                <v-list-item v-for="item in more" :key="item" @click="addItem(item)">
                  {{ item }}
                </v-list-item>
              </v-list>
            </v-menu> -->
          </v-tabs>
        </template>
      </v-app-bar>
    </v-card>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer padless>
      <v-col cols="12">
        <v-row flat tile class="indigo lighten-1 white--text text-center">
          <v-card-text>
            <v-btn v-for="icon in icons" :key="icon" class="mx-4 white--text" icon>
              <v-icon size="24px">
                {{ icon }}
              </v-icon>
            </v-btn>
          </v-card-text>

          <v-card-text class="white--text pt-0"> texto grande</v-card-text>

          <v-divider></v-divider>

          <v-card-text class="white--text">
            {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
          </v-card-text>
        </v-row>
      </v-col>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "DefaultLayout",
  data() {
    return {
      icons: ["mdi-facebook", "mdi-twitter", "mdi-linkedin", "mdi-instagram"],
      currentItem: "tab-Web",
      itemsTab: ["Frequently Asked Questions", "Client Policies", "About us"],
      services: ["Checklist", "Deep Cleaning", "Apartment Cleaning", "postconstruction"],
      more: ["News", "Maps", "Books", "Flights", "Apps"],
      text:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/",
        },
        {
          icon: "mdi-chart-bubble",
          title: "Inspire",
          to: "/inspire",
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js",
    };
  },
};
</script>

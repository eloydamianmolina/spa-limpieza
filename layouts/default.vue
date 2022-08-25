<template>
  <v-app>
    <v-card class="d-flex">
      <v-app-bar fixed app class="rounded-b-xl">
        <v-toolbar-title class="text-h6 text-sm-h4"
          ><v-avatar :tile="true">
            <img :src="require('@/static/vuetify-logo.svg')" alt="logo" /> </v-avatar
          >Clean Company</v-toolbar-title
        >
        <template v-slot:img="{ props }">
          <v-img
            v-bind="props"
            gradient="to top , rgba(100,115,201,.10), rgba(25,32,72,.1)"
          >
          </v-img>
        </template>

        <template v-slot:extension>
          <v-spacer></v-spacer>
          <v-tabs v-model="currentItem" class="">
            <v-menu bottom left open-on-hover>
              <template v-slot:activator="{ on, attrs }">
                <v-btn
                  text
                  class="align-self-center mb-3 ml-sm-16 ml-md-16"
                  v-bind="attrs"
                  v-on="on"
                >
                  Services
                  <v-icon right> mdi-menu-down </v-icon>
                </v-btn>
              </template>

              <v-list class="grey lighten-3">
                <v-list-item
                  v-for="item in services"
                  :key="item.name"
                  :to="'/services/' + item.href"
                >
                  {{ item.name }}
                </v-list-item>
              </v-list>
            </v-menu>
            <v-btn
              class=""
              :area-select="false"
              v-for="item in itemsTab"
              :key="item"
              :to="'/' + item"
              text
              >{{ item }}</v-btn
            >
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
        <v-spacer></v-spacer>
        <div v-if="!$vuetify.breakpoint.mobile">
          <v-btn v-for="icon in icons" :key="icon.icon" class="mx-4" icon>
            <a :href="'https://' + icon.href" target="_blank" rel="noopener noreferrer">
              <v-icon size="24px" color="grey darken-2">
                {{ icon.icon }}
              </v-icon>
            </a>
          </v-btn>
        </div>
      </v-app-bar>
    </v-card>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer padless>
      <v-col cols="12">
        <v-row flat tile class="text-center">
          <v-card-text>
            <v-btn v-for="icon in icons" :key="icon" class="mx-4" icon>
              <v-icon size="24px">
                {{ icon }}
              </v-icon>
            </v-btn>
          </v-card-text>

          <v-card-text class="pt-0"> texto grande</v-card-text>

          <v-divider></v-divider>

          <v-card-text class="">
            {{ new Date().getFullYear() }} — <strong>Clean Company</strong>
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
      icons: [
        { icon: "mdi-facebook", href: "facebook.com" },
        { icon: "mdi-twitter", href: "twitter.com" },
        { icon: "mdi-linkedin", href: "linkedin.com" },
        { icon: "mdi-instagram", href: "instagram.com" },
      ],
      currentItem: "tab-Web",
      itemsTab: ["Frequently Asked Questions", "Client Policies", "About us"],
      services: [
        {
          name: "Apartament Clean",
          href: "apartamentcleaning",
          url: "clearhome2.jpg",
        },
        { name: "Windows Cleaning", href: "windows_cleaning", url: "clean-glass.jpg" },
        { name: "Roof Cleaning", href: "roof_cleaning", url: "roof-cleaning.jpg" },
        {
          name: "Post Construction",
          href: "postconstruction",
          url: "post-construction.jpeg",
        },
        { name: "Garage Cleaning", href: "garage_cleaning", url: "garage_cleaning.jpg" },
      ],
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
<style>
#app {
  /* background: url("~/assets/images/agua.jpg") no-repeat center center fixed !important;
  background-size: cover; */
  background-color: rgb(253, 253, 253);
}
.v-tabs {
  align-items: end;
}
a {
  text-decoration: none;
}
</style>

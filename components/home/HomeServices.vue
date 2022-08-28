<template>
  <v-row class="justify-center lighten-3 pt-5 pb-5">
    <v-col cols="12" class="text-center">
      <p class="text-h2 service">Services</p>
      <v-divider></v-divider>
    </v-col>
    <v-col v-for="n in items" cols="6" sm="2" :key="n.name" class="">
      <v-card hover max-width="250" class="blue lighten-4" :to="'/services/' + n.href">
        <v-img
          :src="require('~/assets/images/' + n.url)"
          aspect-ratio="1"
          class="grey lighten-2"
          gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.2)"
        >
          <template v-slot:placeholder>
            <v-row class="fill-height ma-0" align="center" justify="center">
              <v-progress-circular
                indeterminate
                color="grey lighten-5"
              ></v-progress-circular>
            </v-row>
          </template>
        </v-img>
        <p class="text-center ma-3" v-text="n.name"></p>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      items: [
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
    };
  },
};
</script>

<style>
.service {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
}
</style>

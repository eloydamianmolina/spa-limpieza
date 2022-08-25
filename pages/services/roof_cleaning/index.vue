<template>
  <v-row>
    <v-col cols="12" class="text-center">
      <p class="text-h2 service">Roof Cleaning</p>
      <v-divider></v-divider>
    </v-col>
    <v-col cols="12" sm="6" md="6" xl="4">
      <v-img
        :src="require('@/assets/images/roof-cleaning.jpg')"
        :class="$vuetify.breakpoint.mobile ? 'rounded-r-xl' : 'rounded-lg'"
        contain
        max-width="500"
      >
      </v-img>
    </v-col>
    <v-divider class="mt-5" v-show="!$vuetify.breakpoint.xsOnly" vertical></v-divider>
    <v-col cols="12" sm="6" md="6" xl="6">
      <p class="body-1">
        Our professionals are carefully screened and chosen for both their competence and
        their pristine backgrounds, so you never have to worry about who you are letting
        into your home or whether or not the job will be completed our only standard is
        perfection!
      </p>
      <p class="body-1">
        We deploy only the most eco-friendly options. For example, we use HEPA-friendly
        vacuum cleaners that pick up 99% of the dust in the places we clean. We also stay
        away from anything that can be classified as harmful or toxic products instead, we
        use green, eco-friendly cleaners. You no longer have to worry about harmful
        products being used around your pets or children.
      </p>
      <p class="body-1">
        Our professionals are carefully screened and chosen for both their competence and
        their pristine backgrounds, so you never have to worry about who you are letting
        into your home or whether or not the job will be completed our only standard is
        perfection!
      </p>
      <p class="body-1">
        We deploy only the most eco-friendly options. For example, we use HEPA-friendly
        vacuum cleaners that pick up 99% of the dust in the places we clean. We also stay
        away from anything that can be classified as harmful or toxic products instead, we
        use green, eco-friendly cleaners. You no longer have to worry about harmful
        products being used around your pets or children.
      </p>
    </v-col>

    <v-row justify="center" align="center">
      <!-- <v-col class="mt-6" cols="10"><v-divider></v-divider></v-col> -->
      <v-col cols="12" sm="4" md="4" class="text-center">
        <form-home></form-home>
      </v-col>
    </v-row>

    <!-- <v-col cols="12" sm="6" md="6">
      <v-img
      
        :src="require('@/assets/images/clearhome.jpg')"
        :class="$vuetify.breakpoint.mobile ? 'rounded-r-xl' : 'rounded-lg'"
        contain
        max-width="500"
      >
      </v-img>
    </v-col> -->
  </v-row>
</template>

<script>
import FormHome from "../../../components/home/FormHome.vue";
export default {
  components: { FormHome },
  data() {
    return {};

    FormHome;
  },
};
</script>

<style scoped>
.cardColor {
  background-color: rgba(236, 236, 236, 0.705) !important;
  border-color: white !important;
}
</style>

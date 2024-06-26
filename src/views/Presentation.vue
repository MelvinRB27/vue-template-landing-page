<template>
  <v-card class="container-presentation">
    <div class="container-body-presentation">
      <div>
        <v-card-title class="title-presentation"
          >Lessons and insights</v-card-title
        >
        <v-card-title class="title-2-presentation">from 8 years</v-card-title>
      </div>
      <div>
        <v-card-text class="text-presentation">
          Where to grow your business as a photographer: site or social media?
        </v-card-text>
      </div>
      <v-btn class="btn-presentation">Register</v-btn>
    </div>
    <ilustration-icon />
  </v-card>
</template>

<script>
import IlustrationIcon from "@/icons/IlustrationIcon.vue";
export default {
  components: { IlustrationIcon },
  name: "Presentation",
};
</script>

<style lang="scss" scoped>
@import "@/styles/Presentation.scss";
</style>

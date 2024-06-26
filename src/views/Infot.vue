<template>
  <div class="container-infot">
    <div class="card-infot">
      <CellWithPersonIcon />
      <div>
        <v-card-title class="title">
          How to design your site footer like we did
        </v-card-title>
        <v-card-text class="description">
          Donec a eros justo. Fusce egestas tristique ultrices. Nam tempor,
          augue nec tincidunt molestie, massa nunc varius arcu, at scelerisque
          elit erat a magna. Donec quis erat at libero ultrices mollis. In hac
          habitasse platea dictumst. Vivamus vehicula leo dui, at porta nisi
          facilisis finibus. In euismod augue vitae nisi ultricies, non aliquet
          urna tincidunt. Integer in nisi eget nulla commodo faucibus efficitur
          quis massa. Praesent felis est, finibus et nisi ac, hendrerit
          venenatis libero. Donec consectetur faucibus ipsum id gravida.
        </v-card-text>
        <v-btn class="btn">Learn More</v-btn>
      </div>
    </div>
  </div>
</template>

<script>
import CellWithPersonIcon from "@/icons/CellWithPersonIcon.vue";
export default {
  components: { CellWithPersonIcon },
  name: "Publics",
};
</script>

<style lang="scss" scoped>
@import "@/styles/Infot.scss";
</style>

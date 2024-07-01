<template>
  <v-card class="container-demo">
    <v-card-title class="title-demo">
      Pellentesque suscipit fringilla libero eu.
    </v-card-title>
    <v-btn class="btn">
      <span>Get a Demo</span>
      <ArrowRight :width="20" :height="20" color="white" />
    </v-btn>
  </v-card>
</template>

<script>
import ArrowRight from "@/icons/ArrowRight.vue";
export default {
  components: { ArrowRight },
  name: "Demo",
};
</script>

<style lang="scss" scoped>
@import "@/styles/_variables.scss";

.container-demo {
  background-color: $background-color;
  display: flex;
  align-items: center;
  flex-direction: column;
  gap: 20px;
  padding: 40px;
  border-radius: 0;
  box-shadow: none;
  .title-demo {
    color: $font-color;
    font-size: 60px;
    max-width: 700px;
    text-align: center;
    padding: 0;
    line-height: 1.2;
    word-wrap: break-word;
    overflow-wrap: break-word;
    white-space: normal;
  }
  .btn {
    background: $primary-color;
    color: white;
    text-transform: none;
    font-size: 16px;
    box-shadow: none;
  }
}
</style>

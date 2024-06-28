<template>
  <div class="card-marketing">
    <v-img width="300px" height="300px" :src="image" />
    <v-card class="card-marketing-body">
      <v-card-title class="title-marketing">
        {{ title }}
      </v-card-title>
      <v-btn class="btn">
        <span>Readmore</span>
        <ArrowRight :width="30" :height="30" />
      </v-btn>
    </v-card>
  </div>
</template>

<script>
import ArrowRight from "@/icons/ArrowRight.vue";
export default {
  components: { ArrowRight },
  name: "MarketingCard",
  props: {
    title: {
      type: String,
      default: "#1E88E5",
    },
    image: {
      type: String,
      default: "",
    },
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/MarketingCard.scss";
</style>

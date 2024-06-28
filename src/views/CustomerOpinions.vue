<template>
  <div class="container-infot">
    <div class="card-infot">
      <v-img width="300px" height="300px" src="@/assets/logoTesla.svg" />
      <div class="card-body">
        <v-card-text class="description">
          Maecenas dignissim justo eget nulla rutrum molestie. Maecenas lobortis
          sem dui, vel rutrum risus tincidunt ullamcorper. Proin eu enim metus.
          Vivamus sed libero ornare, tristique quam in, gravida enim. Nullam ut
          molestie arcu, at hendrerit elit. Morbi laoreet elit at ligula
          molestie, nec molestie mi blandit. Suspendisse cursus tellus sed augue
          ultrices, quis tristique nulla sodales. Suspendisse eget lorem eu
          turpis vestibulum pretium. Suspendisse potenti. Quisque malesuada enim
          sapien, vitae placerat ante feugiat eget. Quisque vulputate odio
          neque, eget efficitur libero condimentum id. Curabitur id nibh id sem
          dignissim finibus ac sit amet magna.
        </v-card-text>
        <v-card-title class="title"> Tim Smith </v-card-title>
        <v-card-text class="description">
          British Dragon Boat Racing Association
        </v-card-text>

        <div class="container-logos-opinions">
          <component v-for="logo in logos" :key="logo" :is="logo" />
          <v-btn class="btn">
            <span>Meet all customers</span>
            <ArrowRight />
          </v-btn>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Logo1 from "@/icons/Logo1.vue";
import Logo2 from "@/icons/Logo2.vue";
import Logo3 from "@/icons/Logo3.vue";
import Logo4 from "@/icons/Logo4.vue";
import Logo5 from "@/icons/Logo5.vue";
import Logo6 from "@/icons/Logo6.vue";
import ArrowRight from "@/icons/ArrowRight.vue";
export default {
  components: { Logo1, Logo2, Logo3, Logo4, Logo5, Logo6, ArrowRight },
  name: "CustomerOpinions",
  data() {
    return {
      logos: ["Logo1", "Logo2", "Logo3", "Logo4", "Logo5", "Logo6", "Logo3"],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/CustomerOpinions.scss";
</style>

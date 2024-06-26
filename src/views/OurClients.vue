<template>
  <v-card class="container-our-clients">
    <div>
      <v-card-title class="title-our-clients">Our Clients</v-card-title>
      <v-card-text class="text-our-clients">
        We have been working with some Fortune 500+ clients
      </v-card-text>
    </div>
    <div class="container-logos-clients">
      <component v-for="logo in logos" :key="logo" :is="logo" />
    </div>
  </v-card>
</template>

<script>
import Logo1 from "@/icons/Logo1.vue";
import Logo2 from "@/icons/Logo2.vue";
import Logo3 from "@/icons/Logo3.vue";
import Logo4 from "@/icons/Logo4.vue";
import Logo5 from "@/icons/Logo5.vue";
import Logo6 from "@/icons/Logo6.vue";
export default {
  components: { Logo1, Logo2, Logo3, Logo4, Logo5, Logo6 },
  name: "OurClients",
  data() {
    return {
      logos: ["Logo1", "Logo2", "Logo3", "Logo4", "Logo5", "Logo6", "Logo3"],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/OurClients.scss";
</style>

<template>
  <Presentation />
  <OurClients />
  <Publics />
  <Statistics />
  <Infot />
  <CustomerOpinions />
  <Marketing />
  <Demo />
  <Footer />
</template>

<script>
import OurClients from "@/views/OurClients.vue";
import Presentation from "@/views/Presentation.vue";
import Publics from "@/views/Publics.vue";
import Statistics from "@/views/StatisticsView.vue";
import Infot from "@/views/Infot.vue";
import CustomerOpinions from "@/views/CustomerOpinions.vue";
import Marketing from "@/views/Marketing.vue";
import Demo from "@/views/Demo.vue";

import { defineComponent } from "vue";

export default defineComponent({
  components: {
    OurClients,
    Presentation,
    Publics,
    Statistics,
    Infot,
    CustomerOpinions,
    Marketing,
    Demo
  },
  data() {
    return {
      msg: "Hello, world",
    };
  },
  methods: {
    saludar(newMessage) {
      this.msg = newMessage;
    },
    reset() {
      this.msg = "Hello, world";
    },
  },
});
</script>

<style lang="scss" scoped>
.containerHome {
  display: flex;
  flex-direction: column;
  gap: 16px;
  padding: 20px;
  justify-content: center;
  align-items: center;
}
.divFlex {
  display: flex;
  gap: 16px;
  justify-content: center;
  align-items: center;
}
</style>

<!-- <v-card class="containerHome">
  <div>{{ msg }}</div>
  <div class="divFlex">
    <v-btn @click="reset()"> Default </v-btn>
    <v-btn @click="saludar(`holaaaaaaa`)"> Saludar </v-btn>
  </div>
</v-card> -->

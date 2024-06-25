<template>
  <presentation />
  <our-clients />
  <publics />
  <Statistics />
</template>

<script>
import OurClients from "@/views/OurClients.vue";
import Presentation from "@/views/Presentation.vue";
import Publics from "@/views/Publics.vue";
import Statistics from '@/views/StatisticsView.vue';

import { defineComponent } from "vue";

export default defineComponent({
  components: { OurClients, Presentation, Publics, Statistics },
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

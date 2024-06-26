<template>
  <v-card class="container-statistics">
    <div class="container-body-statistics">
      <div>
        <v-card-title class="title-statistics">Helping a local</v-card-title>
        <v-card-title class="title-2-statistics"
          >business reinvent itself</v-card-title
        >
      </div>
      <div>
        <v-card-text class="text-statistics">
          We reached here with our hard work and dedication
        </v-card-text>
      </div>
    </div>

    <div class="statistics-columns">
      <div
        v-for="(item, index) in column1Items"
        :key="index"
        class="container-statistics-item"
      >
        <component :is="item.icon" />
        <div class="container-statistics-item-text">
          <div class="container-statistics-item-title">{{ item.title }}</div>
          <div class="container-statistics-item-value">{{ item.value }}</div>
        </div>
      </div>

      <div
        v-for="(item, index) in column2Items"
        :key="index"
        class="container-statistics-item"
      >
        <component :is="item.icon" />
        <div class="container-statistics-item-text">
          <div class="container-statistics-item-title">{{ item.title }}</div>
          <div class="container-statistics-item-value">{{ item.value }}</div>
        </div>
      </div>
    </div>
  </v-card>
</template>

<script lang="ts">
import { useRouter } from "vue-router";
import Member2IconVue from "@/icons/Membera2Icon.vue";
import Hands2IconVue from "@/icons/Hands2Icon.vue";
import ClickIconVue from "@/icons/ClickIcon.vue";
import CreditCardIconVue from "@/icons/CreditCardIcon.vue";

interface StatisticsValue {
  title: string;
  value: string;
  icon: any;
}

export default {
  components: {
    Member2IconVue,
    Hands2IconVue,
    ClickIconVue,
    CreditCardIconVue,
  },
  name: "StatisticsView",
  setup() {
    const router = useRouter();

    const statisticsItems: StatisticsValue[] = [
      { title: "Members", value: "2,245,341", icon: Member2IconVue },
      { title: "Clubs", value: "46,328", icon: Hands2IconVue },
      { title: "Event Bookings", value: "828,867", icon: ClickIconVue },
      { title: "Payments", value: "1,926,436", icon: CreditCardIconVue },
    ];

    const half = Math.ceil(statisticsItems.length / 2);
    const column1Items = statisticsItems.slice(0, half);
    const column2Items = statisticsItems.slice(half);

    const navigateTo = (route: string) => {
      router.push(route);
    };

    return {
      column1Items,
      column2Items,
      navigateTo,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/Statistics.scss";
</style>

<template>
  <div class="container-public">
    <div
      :style="{
        textAlign: 'center',
        display: 'flex',
        flexDirection: 'column',
        gap: '10px',
      }"
    >
      <v-card-title class="title-public">
        Manage your entire community in a single system
      </v-card-title>
      <v-card-text> Who is Nextcent suitable for? </v-card-text>
    </div>

    <div class="container-list-cards">
      <v-card
        class="card-list-public"
        v-for="(item, index) in publicItems"
        :key="index"
      >
        <component :is="item.icon" class="icon"></component>
        <v-card-title class="title-card-list"> {{ item.label }} </v-card-title>
        <v-card-text :style="{ textAlign: 'center' }">
          {{ item.description }}
        </v-card-text>
      </v-card>
    </div>

    <div class="card-infot">
      <CellWithPersonsIcon />
      <div>
        <v-card-title class="title">
          The unseen of spending three years at Pixelgrade
        </v-card-title>
        <v-card-text class="description">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed sit amet
          justo ipsum. Sed accumsan quam vitae est varius fringilla.
          Pellentesque placerat vestibulum lorem sed porta. Nullam mattis
          tristique iaculis. Nullam pulvinar sit amet risus pretium auctor.
          Etiam quis massa pulvinar, aliquam quam vitae, tempus sem. Donec
          elementum pulvinar odio.
        </v-card-text>
        <v-btn class="btn">Learn More</v-btn>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import BuildIcon from "@/icons/BuildIcon.vue";
import HandasIcon from "@/icons/HandsIcon.vue";
import MembersIcon from "@/icons/MembersIcon.vue";
import CellWithPersonsIcon from "@/icons/CellWithPersonsIcon.vue";
import { defineComponent } from "vue";
import { useRouter } from "vue-router";

interface PublicItem {
  label: string;
  description: string;
  icon: any;
}

export default defineComponent({
  components: { CellWithPersonsIcon },
  name: "Publics",
  setup() {
    const router = useRouter();

    const publicItems: PublicItem[] = [
      {
        label: "Membership Organisations",
        description:
          "Our membership management software provides full automation of membership renewals and payments",
        icon: MembersIcon,
      },
      {
        label: "National Associations",
        description:
          "Our membership management software provides full automation of membership renewals and payments",
        icon: BuildIcon,
      },
      {
        label: "Clubs And Groups",
        description:
          "Our membership management software provides full automation of membership renewals and payments",
        icon: HandasIcon,
      },
    ];

    const navigateTo = (route: string) => {
      router.push(route);
    };

    return {
      publicItems,
      navigateTo,
    };
  },
});
</script>

<style lang="scss" scoped>
@import "@/styles/Publics.scss";
</style>

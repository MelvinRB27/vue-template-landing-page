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
      <CellWithPersonIcon />
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
import CellWithPersonIcon from "@/icons/CellWithPersonIcon.vue";
import { defineComponent } from "vue";
import { useRouter } from "vue-router";

interface PublicItem {
  label: string;
  description: string;
  icon: any;
}

export default defineComponent({
  components: { CellWithPersonIcon },
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
.container-public {
  color: black;
  display: flex;
  align-items: center;
  flex-direction: column;
  gap: 20px;
  padding: 40px;
  border-radius: 0;
  box-shadow: none;
}

.title-public {
  color: #4d4d4d;
  font-size: 40px;
  max-width: 700px;
  padding: 0;
  text-align: center;
  line-height: 1.2;
  word-wrap: break-word;
  overflow-wrap: break-word;
  white-space: normal;
}
.container-list-cards {
  display: flex;
  width: 90%;
  align-items: center;
  justify-content: space-between;
//   gap: 190px;
}
.card-list-public {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 299px;
  -webkit-box-shadow: 0px 2px 2px 0px rgba(171, 190, 209, 0.2);
  -moz-box-shadow: 0px 2px 2px 0px rgba(171, 190, 209, 0.2);
  box-shadow: 0px 2px 4px 0px rgba(171, 190, 209, 0.2);
}
.title-card-list {
  text-align: center;
  max-width: 250px;
  font-size: 30px;
  word-wrap: break-word;
  overflow-wrap: break-word;
  white-space: normal;
}
.card-infot {
  display: flex;
  align-items: center;
  gap: 100px;
  padding: 0px 40px;
  box-shadow: none;
}

.card-infot div {
  display: flex;
  flex-direction: column;
  align-items: ce;
  gap: 20px;
}

.card-infot .title {
  color: #4d4d4d;
  font-size: 40px;
  max-width: 600px;
  padding: 0;
  line-height: 1.2;
  word-wrap: break-word;
  overflow-wrap: break-word;
  white-space: normal;
}

.card-infot .description {
  color: #4d4d4d;
  max-width: 590px;
  padding: 0;
  line-height: 1.2;
  word-wrap: break-word;
  overflow-wrap: break-word;
  white-space: normal;
}

.btn {
  color: white;
  text-transform: capitalize;
  font-size: 12px;
  background-color: #4caf4f;
  border: 1px solid #4caf4f;
  border-radius: 5px;
  height: 40px;
  width: 100px;
}
</style>

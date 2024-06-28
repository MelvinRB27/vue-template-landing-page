<template>
  <v-card class="container-marketing">
    <div class="div1">
      <v-card-title class="title-marketing"
        >Caring is the new marketing</v-card-title
      >
      <v-card-text class="text-marketing">
        The Nextcent blog is the best place to read about the latest membership
        insights, trends and more. See who's joining the community, read about
        how our community are increasing their membership income and lot's
        more.​
      </v-card-text>
    </div>
    <div class="container-card-markting">
      <MarketingCard
        v-for="(item, index) in marketingItems"
        :key="index"
        :image="item.image"
        :title="item.title"
      />
    </div>
  </v-card>
</template>

<script lang="ts">
import MarketingCard from "@/components/MarketingCard.vue";
import image18 from "@/assets/image18.svg";
import image19 from "@/assets/image19.svg";
import image20 from "@/assets/image20.svg";

interface MarketingItems {
  title: string;
  image: string;
}

export default {
  components: { MarketingCard },
  name: "Marketing",
  setup() {
    const marketingItems: MarketingItems[] = [
      {
        title: "Creating Streamlined Safeguarding Processes with OneRen",
        image:image18,
      },
      {
        title:
          "What are your safeguarding responsibilities and how can you manage them?",
        image:image19,
      },
      {
        title: "Revamping the Membership Model with Triathlon Australia",
        image:image20,
      },
    ];

    return {
      marketingItems,
    };
  },
  data() {
    return {
      test: "test",
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/Marketing.scss";
</style>

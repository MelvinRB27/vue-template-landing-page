<template>
  <v-card class="container-presentation">
    <div class="container-body-presentation">
      <div>
        <v-card-title class="title-presentation"
          >Lessons and insights</v-card-title
        >
        <v-card-title class="title-2-presentation">from 8 years</v-card-title>
      </div>
      <div>
        <v-card-text class="text-presentation">
          Where to grow your business as a photographer: site or social media?
        </v-card-text>
      </div>
      <v-btn class="btn-presentation">Register</v-btn>
    </div>
    <ilustration-icon />
  </v-card>
</template>

<script>
import IlustrationIcon from "@/icons/IlustrationIcon.vue";
export default {
  components: { IlustrationIcon },
  name: "Presentation",
};
</script>

<style lang="scss" scoped>
.container-presentation {
  background-color: #f5f7fa;
  color: black;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 40px 200px;
  border-radius: 0;
  box-shadow: none;
}

.container-body-presentation {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.title-presentation {
  color: #4d4d4d;
  font-size: 48px;
  padding: 0;
  line-height: 50px;
}
.title-2-presentation {
  color: #4caf4f;
  font-size: 48px;
  padding: 0;
  line-height: 50px;
}

.text-presentation {
  padding: 0;
}

.container-presentation .btn-presentation {
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

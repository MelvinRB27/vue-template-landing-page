<template>
  <v-app-bar :elevation="0" :style="{ background: '#f5f7fa' }">
    <v-app-bar-nav-icon class="burgerBar" />
    <div class="container-items-bar">
      <div class="d-flex ga-2 align-center">
        <v-img width="35" height="24" src="@/assets/Icon.svg" />
        <h1>Nextcent</h1>
      </div>
      <v-btn-group class="btn-group-links" color="transparent">
        <v-btn
          v-for="(item, index) in navItems"
          :key="index"
          @click="navigateTo(item.route)"
        >
          {{ item.label }}
        </v-btn>
      </v-btn-group>

      <v-btn-group>
        <v-btn class="btn-login">Login</v-btn>
        <v-btn class="sign-up">Sign Up</v-btn>
      </v-btn-group>
    </div>
  </v-app-bar>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { useRouter } from "vue-router";

export default defineComponent({
  name: "AppBar",
  setup() {
    const router = useRouter();

    const navItems = [
      { label: "Home", route: "/" },
      { label: "Service", route: "/#" },
      { label: "Feature", route: "/#" },
      { label: "Product", route: "/#" },
      { label: "Testimonial", route: "/#" },
      { label: "FAQ", route: "/#" },
    ];

    const navigateTo = (route: string) => {
      router.push(route);
    };

    return {
      navItems,
      navigateTo,
    };
  },
});
</script>

<style lang="scss" scoped>
@import "@/styles/_variables.scss";

.container-items-bar {
  background: #f5f7fa;
  padding: 0px 100px;
  display: flex;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}
.btn-login {
  color: $primary-color;
  background-color: transparent;
  text-transform: capitalize;
}
.sign-up {
  background-color: $primary-color;
  color: white;
  text-transform: capitalize;
  border-radius: 5px;
}
</style>

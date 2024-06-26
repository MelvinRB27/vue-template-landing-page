<template>
  <v-app-bar :elevation="0" :style="{ background: '#f5f7fa' }">
    <v-app-bar-nav-icon class="burgerBar" />
    <div class="container-items-bar">
      <h1>Vuetify</h1>
      <v-btn-group class="btn-group-links" color="transparent">
        <v-btn
          v-for="(item, index) in navItems"
          :key="index"
          @click="navigateTo(item.route)"
        >
          {{ item.label }}
        </v-btn>
      </v-btn-group>

      <v-btn-group color="transparent">
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
      { label: "Service", route: "/service" },
      { label: "Feature", route: "/feature" },
      { label: "Product", route: "/product" },
      { label: "Testimonial", route: "/testimonial" },
      { label: "FAQ", route: "/faq" },
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
.container-items-bar {
  background: #f5f7fa;
  padding: 0px 100px;
  display: flex;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}
.btn-login {
  color: #4caf4f;
  background-color: transparent;
  text-transform: capitalize;
}
.sign-up {
  background-color: #4caf4f;
  text-transform: capitalize;
  border-radius: 5px;
}
</style>

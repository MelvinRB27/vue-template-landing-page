<template>
  <v-app class="app">
    <v-main class="mainContainer">
      <AppBars/>
      <router-view />
    </v-main>
  </v-app>
</template>

<script lang="ts" setup>
//
</script>

<style lang="scss" scoped>
.app {
  display: flex;
  // padding: 40px;
}
</style>

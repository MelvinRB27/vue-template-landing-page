<template>
  <div :style="{ display: 'flex', alignItems: 'center' }">
    <svg
      :width="width"
      :height="height"
      viewBox="0 0 9 9"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M6.02324 6.24222L7.12263 5.14283C7.25301 5.01245 7.25301 4.80106 7.12263 4.67068L6.02324 3.57129M7.02484 4.90676L2.35071 4.90676"
        :stroke="color"
        stroke-width="0.5008"
        stroke-linecap="round"
      />
    </svg>
  </div>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "ArrowRight",
  props: {
    color: {
      type: String,
      default: "#4CAF4F",
    },
    width: {
      type: Number,
      default: 48,
    },
    height: {
      type: Number,
      default: 48,
    },
  },
});
</script>

<style scoped>
/* Tus estilos aquí */
</style>

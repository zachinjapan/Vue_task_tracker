<template>
  <button @click="onClick()" :style="{ background: color }" class="btn">
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "AppButton",
  props: {
    text: {
      type: String,
      default: "Button Text N/A",
    },
    color: {
      type: String,
      default: "blue",
    },
  },
  methods: {
    onClick() {
      console.log("Button clicked!");
    },
  },
};
</script>

<style></style>

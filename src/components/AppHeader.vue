<template>
  <header>
    <h1>{{ title }}</h1>
    <AppButton
      @btn-click="$emit('toggle-add-task')"
      :text="showAddTask ? 'Close' : 'Add Task'"
      :color="showAddTask ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import AppButton from "./AppButton.vue";

export default {
  name: "AppHeader",
  components: {
    AppButton,
  },

  props: {
    title: {
      type: String,
      default: "Header Prop N/A",
    },
    showAddTask: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>

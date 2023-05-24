<template>
  <header>
    <h1>{{ title }}</h1>
    <ButtonComponent
      v-show="homepage"
      @btn-click="$emit('toggle-add-task')"
      :text="showAddTask ? 'Close' : 'Add Task'"
      :color="showAddTask ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import ButtonComponent from "./ButtonComponent.vue";

export default {
  name: "HeaderComponent",
  props: {
    title: String,
    showAddTask: Boolean,
  },
  components: {
    ButtonComponent,
  },
  computed: {
    homepage() {
      if (this.$route.path === "/") {
        return true;
      } else {
        return false;
      }
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

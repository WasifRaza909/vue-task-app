<template>
  <div :key="task.id" v-for="task in tasks">
    <TaskComponent :task="task" />
  </div>
</template>

<script>
import TaskComponent from "./TaskComponent.vue";

export default {
  name: "TasksComponent",
  props: {
    tasks: Array,
  },
  components: {
    TaskComponent,
  },
};
</script>

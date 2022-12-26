<template>
  <div v-for="task in tasks" :key="task.id">
    <SingleTask
      :task="task"
      @delete-task="$emit('delete-task', task.id)"
      @toggle-reminder="$emit('toggle-reminder', task.id)"
    />
  </div>
</template>

<script>
import SingleTask from "./SingleTask";

export default {
  name: "AllTasks",
  props: {
    tasks: Array,
  },
  components: {
    SingleTask,
  },
  emits: ["delete-task", "toggle-reminder"],
};
</script>

<template>
  <header>
    <h1>{{ title }}</h1>
    <ButtonAddTask
      @add-task-toggle="$emit('add-task-toggle')"
      btn_text="Add Task"
    />
  </header>
</template>

<script>
import { ButtonAddTask } from "./";
export default {
  name: "MainHeader",
  props: {
    title: {
      type: String,
      default: "Hello, this is the Main Header",
    },
  },
  components: {
    ButtonAddTask,
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
}

header > * {
  margin-left: 2%;
  margin-right: 2%;
}
</style>

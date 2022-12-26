<template>
  <div :class="[task.reminder ? 'reminder' : '', single_task]">
    <h2>{{ task.text }}</h2>
    <h4>{{ task.day }}</h4>
  </div>
</template>

<script>
export default {
  props: {
    task: Object,
  },
};
</script>

<style scoped>
.single-task {
  background-color: rgb(50, 50, 50);
  color: whitesmoke;
  padding: 0.5em 0em;
  margin: 1em 1em;
  border-radius: 8px;
}

.single_task > * {
  padding-left: 1em;
  text-align: left;
}

.reminder {
  border: 2px solid red;
}
</style>

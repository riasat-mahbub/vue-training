<template>
  <div :class="[task.reminder ? 'reminder' : '', 'single_task']">
    <h2>{{ task.text }}</h2>
    <h4>{{ task.day }}</h4>
    <i class="fa fa-times"> </i>
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
.reminder {
  border-left: 4px solid red;
}

.single_task {
  background-color: rgb(50, 50, 50);
  color: whitesmoke;
  padding: 0.5em 0em;
  margin: 1em 1em;
  border-radius: 8px;
  position: relative;
}

.single_task > * {
  padding-left: 1em;
  text-align: left;
}

.fa-times {
  padding: 1em;
  color: crimson;
  position: absolute;
  right: 0;
  top: 0;
}
</style>

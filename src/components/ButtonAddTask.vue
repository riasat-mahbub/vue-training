<template>
  <button @click="onClick()">
    {{ btn_text }}
  </button>
</template>

<script>
export default {
  name: "ButtonAddTask",
  props: {
    btn_text: {
      type: String,
      default: "Hello, this is a Add Task Button",
    },
    color: {
      type: String,
      default: "#ffffff",
    },
  },
  methods: {
    onClick() {
      let btns = document.getElementsByTagName("button");
      for (let btn of btns) {
        btn.classList.toggle("btn-active");
      }
      this.$emit("add-task-toggle");
    },
  },
};
</script>

<style scoped>
button {
  background-color: rgb(172, 9, 0);
  color: rgb(232, 224, 224);
  border-radius: 8px;
  padding: 1em 5em;
  font-size: large;
  font-weight: 700;
}
.btn-active {
  background-color: rgb(0, 130, 56) !important;
  color: rgb(232, 224, 224);
}
</style>

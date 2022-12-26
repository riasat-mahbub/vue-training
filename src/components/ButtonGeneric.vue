<template>
  <button @click="onClick()" :style="{ background: color }">
    {{ btn_text }}
  </button>
</template>

<script>
export default {
  name: "ButtonGeneric",
  props: {
    btn_text: {
      type: String,
      default: "Hello, this is a Generic Button",
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
      console.log("click");
    },
  },
};
</script>

<style scoped>
button {
  background-color: rgb(40, 40, 40);
  color: rgb(232, 224, 224);
  border-radius: 8px;
  padding: 1em;
}
.btn-active {
  background-color: rgb(100, 100, 100) !important;
  color: rgb(232, 224, 224);
}
</style>

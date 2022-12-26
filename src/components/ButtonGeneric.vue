<template>
  <button :style="{ background: color }">{{ btn_text }}</button>
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
}
</style>

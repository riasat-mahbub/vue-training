<template>
  <button>{{ btn_text }}</button>
</template>

<script>
export default {
  name: "ButtonGeneric",
  props: {
    btn_text: {
      type: String,
      default: "Hello, this is a Generic Button",
    },
  },
};
</script>

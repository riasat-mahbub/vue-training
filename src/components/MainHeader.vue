<template>
  <header>
    <h1>{{ title }}</h1>
  </header>
</template>

<script>
export default {
  name: "MainHeader",
  props: {
    title: {
      type: String,
      default: "Hello, this is the Main Header",
    },
  },
};
</script>

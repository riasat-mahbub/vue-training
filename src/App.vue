<template>
  <MainHeader title="Hello John" />
  <ButtonGeneric btn_text="This is a button" color="rgb(40,40,40)" />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import { ButtonGeneric, MainHeader } from "./components";

@Options({
  components: {
    MainHeader,
    ButtonGeneric,
  },
})
export default class App extends Vue {}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

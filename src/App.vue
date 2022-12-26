<template>
  <h1>Hello World</h1>
  <MainHeader />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import MainHeader from "./components/MainHeader.vue";

@Options({
  components: {
    MainHeader,
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

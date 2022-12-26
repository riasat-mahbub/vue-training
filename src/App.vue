<template>
  <MainHeader title="Hello John" />
  <ButtonGeneric btn_text="This is a button" color="rgb(40,40,40)" />
  <AllTasks :tasks="tasks" />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import { ButtonGeneric, MainHeader, AllTasks } from "./components";

@Options({
  components: {
    MainHeader,
    ButtonGeneric,
    AllTasks,
  },
  data() {
    return {
      tasks: [],
    };
  },
  created() {
    this.tasks = [
      {
        id: 1,
        text: "Hello",
        day: "30th February, 2069",
        reminder: true,
      },
      {
        id: 2,
        text: "k thnx bye",
        day: "30th February, 2069",
        reminder: true,
      },
      {
        id: 3,
        text: "Hello",
        day: "30th August, 2099",
        reminder: true,
      },
    ];
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

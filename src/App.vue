<template>
  <MainHeader
    title="Hello John"
    @add-task-toggle="toggleAddTask"
    :showAddTask="showAddTask"
  />
  <div v-show="showAddTask">
    <AddTask @add-task="addTask" />
  </div>
  <AllTasks
    :tasks="tasks"
    @delete-task="deleteSingleTask"
    @toggle-reminder="toggleReminder"
  />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import { ButtonAddTask, MainHeader, AllTasks, AddTask } from "./components";

@Options({
  components: {
    MainHeader,
    ButtonAddTask,
    AllTasks,
    AddTask,
  },
  data() {
    return {
      tasks: [],
      showAddTask: false,
    };
  },
  methods: {
    addTask(task: any) {
      this.tasks = [...this.tasks, task];
    },
    toggleAddTask() {
      this.showAddTask = !this.showAddTask;
    },
    deleteSingleTask(id: number) {
      this.tasks = this.tasks.filter((task: any) => {
        return task.id !== id;
      });
    },
    toggleReminder(id: number) {
      this.tasks = this.tasks.map((task: any) => {
        if (task.id === id) {
          return { ...task, reminder: !task.reminder };
        } else {
          return task;
        }
      });
    },
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
        reminder: false,
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

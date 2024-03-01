<script>
import { ToDo } from "@dhx/trial-todolist";
import "@dhx/trial-todolist/dist/todo.css";

export default {
  props: ["tasks", "users", "projects"],

  mounted() {
    new ToDo(this.$refs.cont, {
      users: this.users,
      tasks: this.tasks,
      projects: this.projects,
    });
  },
  unmounted() {
    this.$refs.cont.innerHTML = "";
  },
};
</script>

<template>
  <div ref="cont" style="width: 100%; height: 100%"></div>
</template>

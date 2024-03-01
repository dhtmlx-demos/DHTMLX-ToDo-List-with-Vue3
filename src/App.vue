<script>
import ToDo from "./components/ToDo.vue";
import { getData } from "./data";

export default {
  components: { ToDo },
  data() {
    const { users, projects, tasks } = getData();
    return {
      users,
      projects,
      tasks,
    };
  },
};
</script>

<template>
  <ToDo :users="users" :tasks="tasks" :projects="projects" />
</template>

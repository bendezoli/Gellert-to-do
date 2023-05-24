<template>
  <div id="app">
    <h1>What To Do?</h1>
    <TodoList />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import TodoList from "./ToDoList/ToDoList.vue";
export default defineComponent({
  name: "App",
  components: {
    TodoList,
  },
});
</script>

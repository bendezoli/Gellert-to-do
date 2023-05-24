<template>
  <div class="ToDoList">
    <ul>
      <li v-for="(toDo, index) in todos" :key="index">
        {{ toDo }}
        <RemoveToDo v-on:todo-removed="handleTodoRemoved(index)" />
      </li>
    </ul>
    <input type="text" v-model="newTodo" placeholder="Add a new ToDo" />

    <AddToDo v-on:add-item="addItem" />
    <ClearAll v-on:clear-all="clear" />
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import ClearAll from "../components/ClearAll.vue";
import RemoveToDo from "../components/RemoveToDo.vue";
import AddToDo from "../components/AddToDo.vue";

const todos = ref<string[]>([]);
const newTodo = ref("");

function handleTodoRemoved(index: number) {
  todos.value.splice(index, 1);
}

function addItem() {
  console.log("add item");
  if (newTodo.value) {
    todos.value.push(newTodo.value);
    newTodo.value = "";
  }
}

function clear() {
  todos.value = [];
  console.log("delete all");
}
</script>

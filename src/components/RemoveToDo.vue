<template>
  <button @click="removeTodo">x</button>
</template>

<script setup lang="ts">
import { defineEmits } from "vue";
// const emit = defineEmits(["todo-removed"]);

// ez az uj kod amikor megadodik a tipusa a string altal
const emit = defineEmits<{
  "todo-removed": [value: string]; // named tuple syntax
}>();

function removeTodo() {
  emit("todo-removed", "delete-one-item");
}
</script>
<style scoped></style>

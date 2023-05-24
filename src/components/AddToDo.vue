<template>
  <button @click="addTodo">Submit</button>
</template>

<script setup lang="ts">
const emit = defineEmits(["add-item"]);

function addTodo() {
  emit("add-item");
}
</script>

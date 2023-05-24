<template>
  <button @click="clearAll">Clear To Do List</button>
</template>

<script setup lang="ts">
const emit = defineEmits(["clear-all"]);

function clearAll() {
  emit("clear-all");
}

// function removeTodo() {}
</script>

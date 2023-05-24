<template>
  <button @click="removeTodo">x</button>
</template>

<script setup lang="ts">
const emit = defineEmits(["todo-removed"]);

function removeTodo() {
  emit("todo-removed");
}
</script>

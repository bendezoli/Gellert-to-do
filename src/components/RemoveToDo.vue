<template>
  <button @click="removeTodo">x</button>
</template>

<script setup lang="ts">
const emit = defineEmits(["todo-removed"]);

function removeTodo() {
  emit("todo-removed");
}
</script>
<style scoped>
/* ide irod a stylet,
 azert scoped mert csak erre a komponensre ervenyes */
</style>

<template>
  <button @click="addTodo">Submit</button>
</template>

<script setup lang="ts">
import { ref } from "vue";

const emit = defineEmits(["add-item"]);

function addTodo() {
  emit("add-item");
}
</script>

<template>
  <div>
    <h1>Hallo</h1>

    <div  >
      <slot name="name"></slot>
    </div>

    <slot name="age"></slot>
  </div>
</template>

<script setup>
import { ref } from "vue";
const props = defineProps(["user"]);

const isActive = ref(false);
const hasError = ref(false);
</script>

<style scoped>

</style>

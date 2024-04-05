<template>
  <div>
    <h1>Hallo</h1>
    <slot name="name"></slot>
    <slot name="age"></slot>
  </div>
</template>

<script setup>
const props = defineProps(["user"]);
</script>

<style scoped>
.text-red {
  color: red;
}

.text-gray {
  color: black;
}
</style>

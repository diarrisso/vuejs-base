<template>
  <div>
    <h1>Hallo</h1>

    <p>{{ props.user.name }} {{ props.user.age}}</p>
  </div>
</template>

<script setup>
const props = defineProps(["user"]);
</script>

<style scoped></style>

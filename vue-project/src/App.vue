<template>
  <HelloWold :user="user" />
  <input type="text" v-model="user.name" />
  <input type="text" v-model="user.age" />
</template>

<script setup>
import HelloWold from "@/components/HelloWorld.vue";
import { ref } from "vue";


const user = ref({
  name: "Masingacite",
  age: 38,
});
</script>

<style scoped></style>

<template>
  <HelloWold :user="user" />

  <div v-if="user.age > 15">v-if="condition"</div>

  <div v-else>v-else</div>
  <input type="text" v-model="user.name" @input="displayName" />
  <input type="text" v-model="user.age" />
</template>

<script setup>
import HelloWold from "@/components/HelloWorld.vue";
import { ref, reactive } from "vue";

// ref props
const user = ref({
  name: "Masingacite",
  age: 39,
});

const users = reactive({
  name: "Masingacite",
  age: 38,
});

// Reactivite
const displayName = () => {
  console.log("name", users.name, "age", users.age);
};

displayName();
</script>

<style scoped></style>

<template>
  <HelloWold />

  <p>{{ sentence }}</p>

  <input type="text" v-model="name" />
  <input type="text" v-model="age" />
</template>

<script setup>
import HelloWold from "@/components/HelloWorld.vue";
import { computed, ref, watch } from "vue";

const name = ref("Masingacite");
const age = ref(30);

watch(name, (newValue, oldValue) => {
  console.log("newValue", newValue, "oldValue", oldValue);
});

watch(age, (newValue, oldValue) => {
  console.log("newValue", newValue, "oldValue", oldValue);
});


</script>

<style scoped>
.text-bold {
  color: black;
  font-weight: bold;
}

.text-green {
  color: green;
}

.text-red {
  color: red;
}
</style>

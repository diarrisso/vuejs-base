<template>
  <HelloWold />

  <p>{{ sentence }}</p>

  <input type="text" v-model="name" />
  <input type="text" v-model="age" />
</template>

<script setup>
import HelloWold from "@/components/HelloWorld.vue";
import { computed, ref } from "vue";

const name = ref("Masingacite");
const age = ref(30);

const sentence = computed(() => {
  return `Guten Morgen , ich bin ${name.value} und ich bin ${age.value} Jahre alte`;
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

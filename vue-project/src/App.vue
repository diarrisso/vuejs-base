<template>
  <HelloWold @update-name="(name) => display(name)" />
</template>

<script setup>
import HelloWold from "@/components/HelloWorld.vue";
import {ref} from 'vue';

const users = ref(['asins'])

const display = (name) => {

	users.value.push([name])
  console.log("app.vue " + name);
  console.log(users.value);
};
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

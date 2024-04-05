<template>
  <div>
    <h1>Hallo</h1>

    {{ name }}

    <input type="text" v-model="name" @input="handleUpdate" />
  </div>
</template>

<script setup>
import { ref } from "vue";
const props = defineProps(["user"]);
const name = ref("Maingacite");

const emit = defineEmits(["updateName"]);

const handleUpdate = (event) => {
  emit("updateName", event.target.value);
  console.log(event.target.value);
};
</script>

<style scoped></style>

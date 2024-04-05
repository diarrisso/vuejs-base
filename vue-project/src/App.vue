<template>
  <HelloWold>
	<template v-slot:name>
		{{ user.name }}
	</template>
	<template v-slot:age>
		{{user.age }}
	</template>
  </HelloWold>
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

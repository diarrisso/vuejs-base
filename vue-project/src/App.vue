<template>
  <HelloWold>
	<template v-slot:name>
		<div class="text-bold"
		:class="[user.name.length > 10? 'text-red' : 'text-green']">
			{{ user.name }}
		</div>
	</template>
	<template v-slot:age>
		<div class="text-bold"
		:class="[user.age > 0 ? 'text-green' : 'text-red']">
			{{user.age }}
		</div>
		
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

<style scoped>

	.text-bold {
		color: black;
		font-weight: bold;
	}

	.text-green  {

		color: green;
	}

	.text-red {
		color: red;
	}

</style>

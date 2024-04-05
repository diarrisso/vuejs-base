<template>
  <div class="d-flex">
    <div>
        <h1>Todo1</h1>

        <p> {{ todo }}</p>

         <button @click="id++">Next</button>

    </div>
    
    <div>
        <h1>Todo2</h1>

        <p> {{ todo2 }}</p>
        <button @click="id2++">Next</button>
    </div>
  </div>
</template>

<script setup lang="ts">

import {useCounter } from '@/state';

const {
    id: id,
    todo: todo

} = useCounter();

const {
    id: id2,
    todo: todo2

} = useCounter();
</script>

<style scoped>

 .d-flex {

    display: flex;
 }

</style>

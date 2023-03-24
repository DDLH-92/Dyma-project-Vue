<template>
 <ul>
  <template v-for="({prenom, id}, index) of utilisateurs" :key="id">
    <li v-if="prenom != 'Paul'">{{ prenom }}</li>
  </template>
 </ul>
</template>

<script setup lang="ts">
import { reactive } from "vue";

const utilisateurs = reactive( [
  {prenom: 'Jean', id: 1},
  {prenom: 'Paul', id: 2},
  {prenom: 'Pierre', id: 3},
]);

setTimeout(() => {
  utilisateurs.push({prenom: 'Julie', age: 40})
}, 3000);
</script>

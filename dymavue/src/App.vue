<template>
  <h1><span>>Bonjour</span> le monde !</h1>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const fontSize = ref('font-size: 50px;')
const color = ref('color: red;')

</script>


<style scoped lang = "scss">

h1 {
  color: red;
  span {
    color: blue;
  }
}

</style>

<template>
<button @click="toggle = !toggle">Toggle</button>
<h1 v-show="toggle">Bonjour le monde !</h1>
<h2 v-pre>{{ variable1 }}</h2>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const toggle = ref(true);
const variable1 = ref('une valeur');

</script>

<style scoped lang = "scss">


</style>

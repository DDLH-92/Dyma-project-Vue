<template>
  <h2>Count : {{ count }}</h2>
  <button @click="incCount">add</button>
</template>

<script setup lang="ts">
import { ref } from "vue";
import type { Ref } from "vue";


const count = ref(0);

function getRef(num: Ref<number>) {
  num.value++
}

getRef(count)

</script>


<style></style>

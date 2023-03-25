<template>
  <h1>Blog</h1>
  <button @click="count++">Submit</button>
  <p> {{ count }}</p>
</template>

<script lang="ts" setup>
import { onBeforeMount, onBeforeUnmount, onBeforeUpdate, onMounted, onUnmounted, onUpdated, ref } from 'vue';


const count = ref(0);

const intervalId = setInterval(() => {
  console.log('tick');
}, 1000)

onBeforeMount(()=> {
  console.log('on before mounted');
})

onMounted(()=> {
  console.log('mounted');
})

onBeforeUpdate(()=> {
  console.log('on before update');
})

onUpdated(()=> {
  console.log('on updated');
})

onBeforeUnmount(()=> {
  console.log('onBeforeUnmount');
})

onUnmounted(()=> {
  clear interval(intervalId)
  console.log('onUnmounted');
})

</script>

<style lang="scss"></style>

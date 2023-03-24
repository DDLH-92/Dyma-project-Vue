<template>
  <h1>Bonjour {{ user.name }}</h1>
  <h2>Count : {{ state.count }}</h2>
  <button @click="incCount">add</button>
</template>

<script setup lang="ts">
import { nextTick, reactive } from "vue";


const state = reactive ({
  user: {
  name : 'Tintin',
  age : 15
},
count: 0
})

let {user, count } = state;

console.log(count === state.count)

function incCount() {
  user.name = user.name === 'Tintin' ? 'Milou' : 'Tintin'
  state.count++;
  nextTick(() => {
    console.log('tick')
  })
}

</script>


<style></style>

<template>
  <h1 @click="userClick" @mouseenter="userEnter">Hello World !</h1>
  <input @input="userInput($event, 'word')" type="text">
</template>

<script setup lang="ts">

let count = 0;

function userEnter(event: MouseEvent) {
  console.log(event)
}

function userInput(event: Event, str: string) {
  const target = event.target as HTMLInputElement;
  target.value = 'Bonjour';
  console.log(str);
}

</script>


<style></style>

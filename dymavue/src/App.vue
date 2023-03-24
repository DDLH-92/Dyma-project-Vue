<template>
<input @keyup.enter="mykeyup">
</template>

<script setup lang="ts">

function mykeyup() {
  console.log('mykeyup');
}


</script>


<style></style>

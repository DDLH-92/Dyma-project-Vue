<template>
<h1 v-bind="obj">Bonjour monde !</h1>
<input :type="inputType">
</template>

<script setup lang="ts">

const key = 'class';
const h1title = 'montitre2';
const h1id = 'unid2';

const obj = {
  [key ]: h1title,
  'id': h1id
}

const inputType = 'number';
</script>

<style></style>

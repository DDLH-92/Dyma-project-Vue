<template>
</template>

<script setup lang="ts">

interface User {
  name: string,
  age: number | string
}

let user: User | null;

function createUser(name: string): User {
  return {
    name: 'David',
    age: 18
  }
}

user = createUser('David')

user.age

</script>


<style></style>

<template>
</template>

<script setup lang="ts">

const obj = { name: 'Jean', age: 12 };

function render() {
  console.log('Should update template')
}
const proxy = new Proxy(obj, {
  get(obj: any, prop) {
    render();
    return obj[prop];
    }
  });

set(obj: any, prop, value) {
  render ();
  obj[prop] = value;
  return true;
}

proxy.age = 15

console.log(proxy.name);
console.log(proxy.age);

</script>


<style></style>

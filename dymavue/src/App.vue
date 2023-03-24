<template>
  <input type="text" v-model="product.quantity">
<h2>Prix total HT : {{ totalPriceHT }}</h2>
<h2>Prix total TTC : {{ totalPriceTTC }}</h2>
</template>

<script setup lang="ts">
import { computed, reactive, watch, ref } from "vue";

const product = reactive({
  name: 'books',
  quantity: 3,
  priceHT: 10,
  nbrOfModification: 0
})

const price = ref(0);

const totalPriceHT = computed(() => product.priceHT * product.quantity)
const totalPriceTTC = computed (() => product.priceHT * product.quantity * 1.2)

const unwatch = watch ([() => product.quantity, price], (newValue, oldValue) => {
  product.nbrOfModification++;
  console.log(newValue);
  console.log(oldValue);
  unwatch();
})



</script>


<style></style>

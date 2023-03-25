<template>
  <h1>Blog title</h1>
  <p :class="$attrs.class">
    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ratione iure quam tempora velit
    repellat repellendus. Blanditiis cumque perferendis alias deserunt modi ad dolorum rerum nihil!
    Quibusdam blanditiis assumenda neque nesciunt.
  </p>
</template>

<script lang="ts" setup>

defineProps<{
  title: string
}>

</script>

<style lang="scss"></style>

<template>
<Blog v-for="title of titles" :title="title" :key="title"/>
</template>

<script setup lang="ts">

import Blog from './Blog.vue';
import { ref } from 'vue';

const titles = ref(['un titre', '2eme titre', '3eme titre'])

</script>

<template>
  <Link href="/">Index</Link> <br />
  <Link href="/hello">Show</Link>
  <div>The page with timer {{ timer }}</div>
  <slot>Default</slot>
</template>


<script setup>
import { Link } from '@inertiajs/vue3'
import { ref } from 'vue'

const timer = ref(0)
setInterval(() => timer.value++, 1000)
</script>

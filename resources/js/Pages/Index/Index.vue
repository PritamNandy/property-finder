<template>
  <div>Index</div>
  <div>
    The Message is from {{ message }}
  </div>
</template>

<script setup>
import { Link } from '@inertiajs/vue3'
defineProps(['message'])
</script>

<template>
  <Link href="/">Index</Link> <br />
  <Link href="/hello">Show</Link>
  <!-- <div>The page with timer {{ timer }}</div> -->
  <div v-if="flashSuccess" class="success">
      {{ flashSuccess }}
  </div>
  <slot>Default</slot>
</template>


<script setup>
import { computed } from 'vue';
import { Link, usePage } from '@inertiajs/vue3';

// page.props.value.flash.success
const page = usePage();
const flashSuccess = computed(
  () => {
     console.log(page.props.value)
  },
)
// import { ref } from 'vue'

// const timer = ref(0)
// setInterval(() => timer.value++, 1000)
</script>

<style scoped>
  .success {
    background: lightgreen;
    color: #333;
  }
</style>

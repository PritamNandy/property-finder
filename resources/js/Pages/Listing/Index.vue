<template>
    <div>
        <div v-for="listing in listings" :key="listing.id">
            {{ listing.city }}
        </div>
    </div>
</template>

<script setup>
    defineProps({
        listings: Array,
    })
</script>
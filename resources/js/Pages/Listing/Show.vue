<template>
    <div>
        <ListingAddressVue :listing="listing" />
    </div>
</template>

<script setup>
    import ListingAddressVue from "@/components/ListingAddress.vue"
    defineProps({
        listing: Object
    })
</script>
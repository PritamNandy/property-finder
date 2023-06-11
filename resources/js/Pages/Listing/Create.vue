<template>
    <form @submit.prevent="create">
        <div>
            <div>
                <label for="">Beds</label>
                <input type="number" v-model.number="form.beds">
            </div>
            <div>
                <label for="">Baths</label>
                <input type="number" v-model.number="form.baths">
            </div>
            <div>
                <label for="">Area</label>
                <input type="text" v-model.number="form.area">
            </div>
            <div>
                <label for="">City</label>
                <input type="text" v-model="form.city">
            </div>
            <div>
                <label for="">Postcode</label>
                <input type="text" v-model="form.code">
            </div>
            <div>
                <label for="">Street</label>
                <input type="text" v-model="form.street">
            </div>
            <div>
                <label for="">Street NR</label>
                <input type="text" v-model="form.street_nr">
            </div>
            <div>
                <label for="">Price</label>
                <input type="text" v-model.number="form.price">
            </div>
            <div>
                <button type="submit">Create</button>
            </div>
        </div>
    </form>
</template>

<style scoped>
    label {
        margin-right: 2em;
    }

    div {
        padding: 2px;
    }
</style>

<script setup>
    import { useForm } from '@inertiajs/vue3';

    const form = useForm({
        beds: 0,
        baths: 0,
        area: 0,
        city: null,
        code: null,
        street: null,
        street_nr: null,
        price: 0,
    })

    const create = () => form.post('/listing')
</script>
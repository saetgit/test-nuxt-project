<template>
    <div class="container mx-auto">
        <Baner />
        <Search />
        <h3 class="text-3xl font-bold mt-8">What do you want done for you?</h3>
        <div class="grid grid-cols-5 gap-4 mt-4">
            <Category v-for="(category, index) in categories" :key="index" :category="category" />
        </div>
        <div class="grid grid-cols-2 gap-4 mt-8">
            <Card v-for="(card, index) in cards" :key="index" :card="card" />
        </div>
        <div class="flex justify-center">
            <Pagnation />
        </div>
    </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import axios from 'axios';

const categories = ref([]);
const cards = ref([]);

onMounted(async () => {
    try {
        const categoriesResponse = await axios.get("categories.json");
        categories.value = categoriesResponse.data;

        const cardsResponse = await axios.get("cards.json");
        cards.value = cardsResponse.data;
    } catch (error) {
        console.error('Error fetching data:', error);
    }
});
</script>
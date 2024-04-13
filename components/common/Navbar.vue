<template>
    <div class="flex items-center justify-between h-[110px] shadow-lg p-4">
        <img src="@/assets/image/icon.png" class="w-[400px]" />
        <ul class="flex gap-4 mx-[50px]">
            <li v-for="(item, index) in menuItems" :key="index" :class="{ active: activeItem === index }"
                @click="activeItem = index" class="px-4">{{ item }}</li>
        </ul>
        <div class="flex items-center justify-end  bg-gray-100 rounded-md px-4 ">
            <img src="@/assets/svg/search.svg" alt="search"  />
            <input class="border-none px-4 py-2 bg-transparent" type="text" />
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';
const menuItems = ref(['Home', 'Employers', 'Freelancers']);
const activeItem = ref(0);
</script>

<style scoped>
.active {
    border-right: 2px solid #f29daf;
}
</style>
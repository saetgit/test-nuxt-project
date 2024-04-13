<template>
    <footer class="bg-white shadow-lg  border-2  py-8">
        <div class="container mx-auto">
            <div class="grid grid-cols-1 md:grid-cols-5 gap-4">
                <div class="text-center">
                    <img src="@/assets/image/icon-footer.png" alt="icon" class="" />
                    <p class="mt-4 text-justify">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
                        labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
                        laboris nisi ut aliquip ex ea commodo consequat.
                    </p>
                </div>

                <div v-for="(column, index) in dynamicColumns" :key="index" class="text-center">
                    <h3 class="text-lg font-semibold">{{ column.title }}</h3>
                    <ul class="mt-4">
                        <li v-for="(subItem, subIndex) in column.subItems" :key="subIndex" class="mb-2">{{ subItem }}
                        </li>
                    </ul>
                </div>

                <div class="text-center">
                    <h3 class="text-lg font-semibold">Column 5</h3>
                    <ul class="mt-4">
                        <li class="mb-2">Item 1</li>
                        <li class="mb-2">Item 2</li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<script setup>
import { ref } from 'vue';

const dynamicColumns = ref([
    {
        title: 'Community',
        subItems: ['Events', 'Mentoring','Jobs','Free Lancering','Learn Drop Shipping']
    },
]);
</script>
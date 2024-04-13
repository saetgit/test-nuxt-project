<template>
    <div class="container mx-auto mt-8">
        <div class="grid grid-cols-2 gap-4">
            <div class="relative">
                <label for="selection1"
                    class="text-[#332324] text-lg font-bold mb-2 absolute top-[-16px] bg-white left-4">Select
                    Service</label>
                <select class="border border-[#c3866b] bg-white w-full outline-none h-14 rounded-lg text-[#332324] px-4"
                    id="selection1" v-model="selectedOption1">
                    <option v-for="option in options" :key="option.value" :value="option.value"
                        class="border border-[#c3866b]  w-full outline-none h-12 px-4 text-[#332324]">{{ option.label }}
                    </option>
                </select>
            </div>
            <div class="relative">
                <label for="selection2"
                    class="text-[#332324] text-lg font-bold mb-2 absolute top-[-16px] bg-white left-4">Type:</label>
                <select id="selection2" v-model="selectedOption2"
                    class="border border-[#c3866b] bg-white w-full outline-none h-14 rounded-lg text-[#332324]">
                    <option v-for="option in options" :key="option.value" :value="option.value" class="text-[#332324] ">
                        {{ option.label }}</option>
                </select>
            </div>
        </div>
        <div class="mt-4 flex items-center">
            <input type="checkbox" id="checkbox" v-model="isChecked"
                class="h-5 w-5 bg-[#c3866b] border border-[#c3866b] rounded-sm accent-[#332324]">
            <label for="checkbox" class="ml-4 text-[#332324]">Project matching my skills</label>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const options = [
    { label: 'Webdesign 1', value: 'Webdesign-1' },
    { label: 'Webdesign 2', value: 'Webdesign-2' },
    { label: 'Webdesign 3', value: 'Webdesign-3' },
    { label: 'Webdesign 4', value: 'Webdesign-4' },
];

const selectedOption1 = ref('Webdesign-1');
const selectedOption2 = ref('');
const isChecked = ref(false);
</script>

<style scoped>
.container {
    padding: 20px;
}

label {
    display: block;
    margin-bottom: 5px;
}
selection option:hover{
    background-color:red !important
}
</style>
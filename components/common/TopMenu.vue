<template>
    <div class="flex items-center bg-[#1b51a1] text-white h-[70px]">
        <div class="container mx-auto justify-between flex items-center">
            <ul class="flex">
                <li v-for="(item, index) in menuItems" :key="index">
                    <template v-if="index !== 0">
                        <span class="separator">|</span>
                    </template>
                    {{ item }}
                </li>
            </ul>
            <ul class="flex">
                <li>
                    <img src="../../static/icon/user-add.png" class="ml-2 w-5"/>
                </li>
                <li>
                    <span class="separator">|</span>
                </li>
                <li>
                    <img src="../../static/icon/user-icon.png" class="w-5"/>
                </li>
            </ul>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const menuItems = ref(['BPMS Home Page', 'About US']);
</script>

<style scoped>
.separator {
    padding: 0 10px;
    color: white;
}
li{
    cursor: pointer;
}
</style>

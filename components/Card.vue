<template>
    <div class="bg-white p-8 rounded-lg  shadow-lg z-10 border-2 hover:border-2 hover:border-[#cc00ff] ">
        <div class="flex justify-between mb-8">
            <p class="font-bold text-lg text-[#d99c81] text-[20px]">{{ card.title }}</p>
            <div class="flex justify-between items-center mt-2">
                <div>
                    <span v-if="card.status.diferent"
                        class="bg-[#efd0f7] text-[#d01afe] font-semibold px-2 py-3 rounded-lg mr-2">Different</span>
                    <span v-if="card.status.Fulltime"
                        class="bg-[#d0e8da] text-[#4ebc79] font-semibold  px-2 py-3 rounded-lg mr-2">Fulltime</span>
                    <span v-if="card.status.Emergency"
                        class="bg-[#e9d0d0] text-[#ac0d0d] font-semibold px-2 py-3 rounded-lg mr-2">Emergency</span>
                </div>
            </div>
        </div>
        <div class="mt-8 text-[20px]">
            <p>{{ card.description }}</p>
        </div>
        <div class="flex mt-8">
            <span v-for="(tag, index) in card.tags" :key="index"
                class="bg-[#fff8f6] text-[#d99c81] px-2 py-1 rounded-lg mr-2">{{ tag }}</span>
        </div>
        <div class="flex items-center mt-8 bg-[#f7e3d0] text-[#ff7a00] p-2 w-[340px] rounded-lg">
            <img src="@/assets/svg/info-circle.svg" alt="info" class="mr-2" />
            <p>The price is of the highest importance</p>
        </div>
        <div class="flex justify-between mt-4">
            <div class="flex space-x-2 items-center ">
                <img src="@/assets/svg/clock.svg" alt="clock" class="w-5" />
                <span>{{ card.time }} hours ago</span>
                <img src="@/assets/svg/user-square.svg" alt="user" class="w-5" />
                <span>{{ card.offer }} offer</span>
            </div>
            <button
                class="p-4 text-lg border-2 border-[#c3866b] text-[#c3866b] font-bold rounded-lg focus:outline-none hover:text-white hover:bg-[#c3866b]">
                Check and Submit an offer
            </button>
        </div>

    </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps(['card']);
</script>
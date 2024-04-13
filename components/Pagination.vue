<template>
  <div class="pagination flex justify-center mt-8">
    <span
      v-for="(page, index) in totalPages"
      :key="index"
      @click="setCurrentPage(page)"
      :class="{ ' text-[#9f9898]': currentPage === page }"
      class="cursor-pointer px-4 py-2 text-xl  mx-2 hover:text-[#332324]"
    >
      {{ page }}
    </span>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  currentPage: {
    type: Number,
    required: true,
  },
  totalPages: {
    type: Number,
    required: true,
  },
});

</script>

<style scoped>
</style>

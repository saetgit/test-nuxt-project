<template>
    <div class="mt-4 flex justify-between">
        <div >
            <button v-for="pageNumber in 4" :key="pageNumber" @click="goToPage(pageNumber)"
                :class="{ 'bg-gray-200': currentPage !== pageNumber, 'bg-blue-500 text-white': currentPage === pageNumber }"
                class="px-4 py-2 rounded-lg mx-2">{{ pageNumber }}</button>
        </div>
    </div>
</template>
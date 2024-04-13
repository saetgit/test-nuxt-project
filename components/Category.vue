<template>
    <div class="mt-8">
        <div
            class="flex items-center bg-[#fcfcfc] shadow-lg rounded-lg z-10 border-2 border-[#f0efef] p-4 hover:border-[#c3866b] cursor-pointer">
            <div :style="{ backgroundColor: category.bgColor }" class="w-8 p-1 rounded-lg">
                <img :src="category.imageUrl" alt="Category Image" />
            </div>
            <div class="ml-4">
                <p>{{ category.title }}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['category']
};
</script>
<template>
    <div>
      <div v-for="(category, index) in categories" :key="index" :style="{ backgroundColor: category.bgColor }">
        <div>
          <img :src="require(category.imageUrl)" alt="Category Image" />
        </div>
        <div>
          <p>{{ category.title }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: ['categories']
  };
  </script>
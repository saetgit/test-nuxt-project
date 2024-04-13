<template>
    <div class="container mx-auto">
      <Baner />
      <Search />
      <h3>What do you want done for you?</h3>
      <Category :categories="categories" />
    </div>
  </template>
  
  <script>
  export default {
    async fetch() {
      const response = await fetch('/data/db.json');
      const data = await response.json();
      return { categories: data.categories };
    }
  };
  </script
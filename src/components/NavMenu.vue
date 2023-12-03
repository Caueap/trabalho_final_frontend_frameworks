<template>
     <nav>
    <div class="container display-flex align-items-center justify-content-space-between pt-16 pb-16">
      <a v-for="category in categories" :key="category.id" :href="`/${category.name}`">{{ category.name }}</a>
    </div>
  </nav>
</template>

<script>
export default {
    name: 'NavMenu',
    data() {
    return {
      categories: []
    }
  },
  methods: {
    getCategories() {
      fetch('https://api.escuelajs.co/api/v1/categories')
        .then(response => response.json())
        .then(data => {
          this.categories = data.slice(0, 5); // Limit to the first 5 categories
        })
        .catch(error => {
          console.log('error', error);
        });
    }
  },
  mounted() {
    this.getCategories();
  }    
}
</script>

<style lang="scss" scoped>

</style>
<template>
    <div class="categorias pt-32 pb-64">
    <div class="container">
      <h3>Categorias</h3>
      <div class="display-flex gap-8 text-align-center pt-16 pb-16">
        <div v-for="category in categories" :key="category.id">
            <img :src="category.image" :alt="category.name">
            <a href="`/${category.name}`">{{ category.name }}</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'CategoriesComponent',
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
                this.categories = data.slice(0, 5);
            })
            .catch(
                error => {
                    console.log('erro', error)
                }
            )
        }
    },
    mounted() {
        this.getCategories()
    }     
}
</script>

<style lang="scss" scoped>

</style>
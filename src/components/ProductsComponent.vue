<template>
  <div class="produtos pt-32 pb-64">
    <div class="container">
      <h3>Produtos</h3>
      <div class="lista-produtos display-flex align-items-center flex-wrap-wrap gap-16">
        <div v-for="product in products" :key="product.id" class="produto">
          <img :src="product.images[0]" :alt="product.title">
          <div class="detalhes">
            <p class="nome-produto">{{ product.title }}</p>
            <p class="categoria">{{ product.category.name }}</p>
            <p class="preco">R$ {{ product.price.toFixed(2) }}</p>
            <button :class="{ 'no-carrinho': product.addedToCart, 'carrinho': !product.addedToCart }"
              @click="addToCart(product)">
              {{ product.addedToCart ? 'Adicionado' : 'Adicionar ao Carrinho' }}
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductsComponent',
  data() {
    return {
      products: []
    }
  },
  methods: {
    getProducts() {
      fetch('https://api.escuelajs.co/api/v1/products')
        .then(response => response.json())
        .then(data => {
          this.products = data.slice(0, 16);
        })
        .catch(error => {
          console.error('Error fetching products:', error);
        });
    },
  },
  mounted() {
    this.getProducts()
  }

}
</script>

<style scoped>
.lista-produtos {
  display: flex;
  flex-wrap: wrap;
}

.produto {
  width: 25%; 
  
}

.produto-img {
  max-width: 100%; 
  height: auto; 
}

</style>
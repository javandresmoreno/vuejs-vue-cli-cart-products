<template>
    <main class="wrapper">
        <h1>Products</h1>

        <div class="card-container">
            <ProductCard
                class="card"
                v-for="(product, index) in inventory.slice(0)"
                :key="product.id"
                :index="index"
                :product="product"
                :addToCart="addToCart"
            />
        </div>
    </main>
</template>

<script>
import ProductCard from '../components/ProductCard.vue'

export default {
  props: ['inventory', 'addToCart'],
  components: {
    ProductCard
  }
}
</script>

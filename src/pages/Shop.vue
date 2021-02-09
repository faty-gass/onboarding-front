<template>
  <q-page>
    <h2>Liste de produits</h2>
    <div class="flex">
      <Product
        v-for="(item, idx) in products"
        :key="idx"
        :name="item.product"
        :description="item.desc"
        :price="item.price"
        :img="item.img"
      />
    </div>
  </q-page>
</template>

<script>
import Product from "components/Product.vue";

export default {
  components: {
    Product
  },

  data() {
    return {
      productList: []
    };
  },

  computed: {
    products() {
      return this.$store.state.products.allProducts;
    }
  }
};
</script>

<style></style>

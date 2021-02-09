<template>
  <q-page class="q-ma-lg">
    <h2>Liste de produits</h2>
    <div class="row ">
      <div
        class="col-12 col-md-4 q-pa-md"
        v-for="(item, idx) in products"
        :key="idx"
      >
        <Product
          :name="item.product"
          :description="item.desc"
          :price="item.price"
          :img="item.img"
        />
      </div>
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

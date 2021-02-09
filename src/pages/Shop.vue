<template>
  <q-page class="q-ma-lg">
    <h2>Liste de produits</h2>
    <div class="row q-gutter-xl q-mx-auto">
      <Product
        v-for="(item, idx) in products"
        :key="idx"
        :name="item.product"
        :description="item.desc"
        :price="item.price"
        :img="item.img"
        class="col-12 col-md "
        style="min-width : 25vw; max-width : 80vw"
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

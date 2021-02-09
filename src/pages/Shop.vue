<template>
  <q-page>
    <h2>Liste de produits</h2>
    <div class="flex">
      <Product
        name="Produit 1"
        price="20 EUR"
        description="description du produit 1"
        img="https://cdn.quasar.dev/img/mountains.jpg"
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
  }
};
</script>

<style></style>

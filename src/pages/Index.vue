<template>
  <q-page class="flex justify-around items-start">
    <AddProduct />
    <div>
      <router-link to="/shop">
        <h2>Voir les produits</h2>
      </router-link>
    </div>
  </q-page>
</template>

<script>
import AddProduct from "components/AddProduct.vue";

export default {
  name: "PageIndex",
  components: {
    AddProduct
  }
};
</script>

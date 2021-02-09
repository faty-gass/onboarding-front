<template>
  <q-page class="flex flex-center">
    <AddProduct />
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

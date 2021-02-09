<template>
  <q-page>
    <h2>Ajouter un produit</h2>

    <q-form @submit="onSubmit" @reset="onReset" class="q-gutter-md">
      <q-input
        filled
        v-model="name"
        label="Product Name *"
        lazy-rules
        :rules="[val => (val && val.length > 0) || 'This field is mandatory']"
      />

      <q-input
        filled
        v-model="price"
        label="Price *"
        lazy-rules
        :rules="[val => (val && val.length > 0) || 'This field is mandatory']"
      />
      <q-input
        filled
        autogrow
        v-model="description"
        label="Description *"
        lazy-rules
        :rules="[val => (val && val.length > 0) || 'This field is mandatory']"
      />
      <q-input
        filled
        autogrow
        v-model="img"
        label="Image *"
        hint="add the image url"
        lazy-rules
        :rules="[val => (val && val.length > 0) || 'This field is mandatory']"
      />

      <div>
        <q-btn label="Submit" type="submit" color="primary" />
        <q-btn
          label="Reset"
          type="reset"
          color="primary"
          flat
          class="q-ml-sm"
        />
      </div>
    </q-form>
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      name: null,
      price: null,
      description: null,
      img: null
    };
  },

  methods: {
    onSubmit() {
      let newProd = {
        product: this.name,
        price: this.price,
        desc: this.description,
        img: this.img
      };
      console.log(newProd);
      this.$store.commit("products/addProduct", newProd);
    },

    onReset() {
      this.name = null;
      this.price = null;
      this.description = null;
      this.img = null;
    }
  }
};
</script>

<style></style>

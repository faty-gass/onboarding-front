<template>
  <q-card class="my-card">
    <img :src="img" />

    <q-card-section>
      <div class="text-h6">{{ name }}</div>
      <div class="text-subtitle2">{{ price }}</div>
    </q-card-section>

    <q-card-section class="q-pt-none">
      {{ description }}
    </q-card-section>
  </q-card>
</template>

<script>
export default {
  props: {
    name: String,
    price: String,
    img: String,
    description: String
  }
};
</script>

<style></style>

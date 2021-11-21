<template>
  <v-card>
    <v-card-text>
      <v-text-field
          v-model="productTitle"
      >Product title</v-text-field>
      <v-text-field
          v-model.number="productPrice"
      >Product price</v-text-field>
      <v-text-field
          v-model="productDescription"
      >Product description</v-text-field>
      <v-text-field
          v-model="productImgUrl"
      >Product img url</v-text-field>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: "ProductEditSection",
  data: () => ({
    productTitle: '',
    productPrice: null,
    productDescription: '',
    productImgUrl: '',
  }),
}
</script>

<style scoped>

</style>
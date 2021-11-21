<template>
  <v-card>
    <v-card-text>
      <v-text-field
          ref="title"
          v-model="productTitle"
      >Product title</v-text-field>
      <v-text-field
          ref="price"
          v-model.number="productPrice"
      >Product price</v-text-field>
      <v-text-field
          ref="description"
          v-model="productDescription"
      >Product description</v-text-field>
      <v-text-field
          ref="imgUrl"
          v-model="productImgUrl"
      >Product img url</v-text-field>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: "ProductEditSection",
  data: () => ({
    productTitle: '', //kaip gauti is products array value?
    productPrice: null,
    productDescription: '',
    productImgUrl: '',
  }),
  props: {
    title: {
      type: String,
      required: true,
    },

  },
  methods: {
    setNewValue() {
      this.productTitle = this.$refs.title.value;
      this.productPrice = this.$refs.price.value;
      this.productDescription = this.$refs.description.value;
      this.productImgUrl = this.$refs.imgUrl.value;
    }
  }
}
</script>

<style scoped>

</style>
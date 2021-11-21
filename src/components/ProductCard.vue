<template>
  <v-card
      class="mx-auto"
      max-width="500"
      heigt="500"

  >
    <v-img
        height="200px"
        :src="img"
    ></v-img>
    <v-card-title
    class="mb-8">
      {{ title }}
    </v-card-title>
    <v-card-text>
      {{ description }}
      {{ price }}
    </v-card-text>
      <v-btn>
        Add to cart
      </v-btn>
  </v-card>

</template>

<script>
export default {
  name: "ProductCart",
  props: {
    img: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    price: {
      type: Number,
      required: true,
    },
  },
};
</script>

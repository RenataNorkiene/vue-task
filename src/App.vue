<template>
  <div>
    <v-row>
      <v-col
          cols="12"
          md="4"
          v-for="(product, productIndex) in products"
          :key="productIndex"
      >
        <product-card :price="product.price"
                      :description="product.description"
                      :title="product.title"
                      :img="product.img"
        ></product-card>
      </v-col>
    </v-row>
    <v-select
        @change="showOldData"
        label="Select product"
        :items="products.title"
        :item-value="title"
        :item-text="title"
    ></v-select>
    <product-edit-section
        v-if="showProductEditSection"
    ></product-edit-section>
  </div>
</template>

<script>
import ProductCard from "@/components/ProductCard";
import ProductEditSection from "@/components/ProductEditSection";

export default {
  name: 'App',

  components: {
    ProductEditSection,
    ProductCard,
  },

  data: () => ({
    showProductEditSection: false,
    products: [
      {
        title: "Personalized Wooden Wireless Cell Phone Chargers",
        description: "Charging your phone is quick and easy with our gorgeous personalized wooden wireless chargers! Made with premium, high-quality wood, these wireless chargers are beautiful to look at and so easy to use. Simply connect the wireless charger to a power source and place your phone on top of the charger. Your wireless-compatible phone will begin to charge automatically without needing to be connected to the charger. These wooden chargers look beautiful on your nightstand, desk, or countertop, yet fit easily into your purse or pocket to take with you on the go. Choose from three beautiful wood choices and select a design that fits your style and then simple add a name for personalization. You'll love having such a unique charger sitting near you anywhere you charge your phone. These make excellent gifts for all your friends and family. Everyone loves opening a tech-savvy, personalized gift!",
        price: 35.45,
        img: 'https://cdn.shopify.com/s/files/1/0399/1937/products/WirelessCharger_Group_staged.jpg?v=1572985912',
      },
      {
        title: "Manuel LorenzPersonalized Monogram Throw Pillow Covers",
        description: "Get current with home décor trends by adding a classic and beautiful monogram throw pillow cover to any room in your home! Place this decorative pillow on a couch, chair, bench, or bed to accent furniture pieces or bedding. This monogrammed accent throw pillow will certainly stand out and add the finishing touch to your room. Each design is timeless, making it simple to incorporate into your existing home décor. Printed on high-quality washable fabric and using UV fade resistant ink, these pillow covers are a generous 18' x 18' size and feature a zipper opening for a finished appearance and to allow easy insertion and removal of a pillow insert (sold separately). Choose between seven Qualtry-exclusive designs and add a name for personalization. Grab yours today and remember that they make a fabulous wedding, housewarming, birthday, holiday, or neighbor gift for those near and dear to you.",
        price: 22.15,
        img: 'https://cdn.shopify.com/s/files/1/0399/1937/products/staged-1_b233b2a8-7b06-4777-b1c4-e379914d0f1c.jpg?v=1564587947',
      },
      {
        title: "Personalized Halloween Lanterns",
        description: "Our Personalized Halloween Lanterns are the perfect way to spook up your house this Halloween! Choose from several designs, and personalize your lantern any way you choose! These are not only great for your home, but make fantastic neighbor and friend gifts as well. You can also choose to add candles to your purchase so you're sure to have everything you need to spook up your Halloween!",
        price: 44.32,
        img: 'https://cdn.shopify.com/s/files/1/0399/1937/products/Halloween_Lanterns_Image_1.jpg?v=1523489109'
      },
      {
        title: "Personalized Hickory Keystone Handled Cutting Boards",
        description: "Cut and serve in style with our personalized Keystone Handled Cutting Board collection. This gorgeous solid wood cutting board brings the beauty of natural hickory to the kitchen. Its broad flat surface makes it perfect for cutting and the elongated handle makes serving comfortable for any host or hostess. Use the loop in the handle for a beautiful kitchen hanging display. Choose from two sizes and four personalized designs to fit your style and add a name and your design will be expertly laser engraved to stand the test of time. Also available is a classic single-letter monogram without a name.",
        price: 58.59,
        img: 'https://cdn.shopify.com/s/files/1/0399/1937/products/1Campbelllightmainstaged.jpg?v=1616091779'
      },
    ],
  }),
  methods: {
    showOldData(event) {
      this.title = event.title.value;
      this.showProductEditSection = true;
    }
  }
};
</script>

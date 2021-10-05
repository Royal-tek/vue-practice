<template>
  <div class="home">
    <div class = "product-cards-container">
      <productdescriptiondrawer 
      :product="product"
      :active="active.product_drawer"/>

      <productsummarycard
      v-for= "product in item"
      :key = "product.id"
      :product="product"
      v-on:view-product= "viewProduct($event)"/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import items from '../data/item.js'
import productsummarycard from '../components/products/ProductSummaryCard.vue'
import productdescriptiondrawer from '../components/products/ProductDescriptionDrawer.vue'

export default {
  name: 'Home',
  components: {
    productsummarycard,
    productdescriptiondrawer
  },
  data(){
    return{
      item : items,
      product : null,
      active: {
        product_drawer : true
      }
    }
  },
  methods : {
    viewProduct(product){
      this.product = product
    }
  }
}
</script>

<style lang = "scss">
.product-cards-container{
  display: flex;
  flex-wrap : wrap;
  justify-content:center;
}

</style>
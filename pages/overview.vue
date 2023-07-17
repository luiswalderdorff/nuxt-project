<template>
  <section style="background-color: #eee;">
    <div class="container py-5">
      <h4 class="text-center mb-5"><strong>Product listing</strong></h4>

      <div class="row">
        <div class="col-lg-4 col-md-12 mb-4 position-relative" v-for="product in products" :key="product.id">
          <nuxt-link :to="`/details/${product.id}`">
            <img :src="product.thumbnail"
                 class="w-100 bg-image hover-zoom ripple shadow-1-strong rounded"/>
            <h5 class="mb-0 product-price"><span class="badge bg-light text-dark mb-2 mt-2">${{ product.price }}</span></h5>
          </nuxt-link>
        </div>

      </div>

    </div>
  </section>
</template>

<script>
export default {
  data(){
    return{
      products: [],
    }
  },
  async created(){
    const response = await fetch('https://dummyjson.com/products');
    const responseJSON = await response.json();
    this.products = responseJSON.products;
    console.log(this.products)
  }
};
</script>
<style scoped>
img {
  object-fit: cover;
  width: 100%;
  height: 250px;
}

.product-price {
  position: absolute;
  top: 10px;
  left: 22px;
}
</style>

<template>
  <section class="py-5">
    <div class="container px-4 px-lg-5 my-5">
      <div class="row gx-4 gx-lg-5 align-items-center">
        <div class="col-md-6">
          <img class="card-img-top mb-5 mb-md-0"
                                   :src="product.thumbnail" alt="..."/>
        </div>
        <div class="col-md-6">
          <div class="small mb-1">Stock: {{ product.stock }}</div>
          <h1 class="display-5 fw-bolder">{{ product.title }}</h1>
          <div class="fs-5 mb-5">
            <span>${{ product.price }}</span>
          </div>
          <p class="lead">{{ product.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data(){
    return {
      product: {},
    }
  },
  async created(){
    const route = useRoute();
    const id = route.params.id;
    const response = await fetch('https://dummyjson.com/products/' + id);
    this.product = await response.json();
  },
};
</script>
<style>

</style>
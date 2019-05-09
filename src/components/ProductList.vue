<template>
  <div class="cards">
    <div class="card" v-for="product in products" v-bind:key="product.id">
      <img class="product" v-bind:src="product.image" v-bind:alt="product.name" />
      <h3>{{product.name}}</h3>
      <p>{{product.description}}</p>
      <a href="#" v-on:click="addToCart(product, $event)">
        {{product.price}}
        <font-awesome-icon icon="cart-plus" size="1x" />
      </a>
    </div>
  </div>
</template>

<script>

  export default {
    props: ['products'],
    components: {

    },
    methods: {
      addToCart:function (product, e) {
        e.preventDefault()
        this.$emit('add-to-cart', product);
      }
    }
  }
</script>

<style scoped>
  img.product {
    width:180px;
    height: 130px;
  }
  p {
    min-height: 66px
  }
</style>

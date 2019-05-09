<template>
  <div>
    <cart-icon/>
    {{cart.length}}
  </div>
</template>

<script>
import CartIcon from "./CartIcon.vue";
export default {
  props: ["cart"],
  components: {
    CartIcon
  },
  methods: {}
};
</script>

<style scoped>
div {
  font-size: 0.9rem;
  text-align: right;
  margin-top: 10px;
  margin-right: 15px;
  position: -webkit-sticky;
  position: sticky;
  top: 10px;
}
</style>

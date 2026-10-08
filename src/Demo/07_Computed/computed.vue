<script setup>
import { reactive, computed } from "vue";
const cart = reactive([
  { name: "lait", prix: 1000, quantity: 2 },
  { name: "fromage", prix: 2000, quantity: 1 },
  { name: "chocolat", prix: 1500, quantity: 3 },
]);
const total =computed(function () {
return cart.reduce((acc, product) => acc + product.prix * product.quantity, 0)
});
</script>

<template>
  <section class="card">
    <h2>11 - computed()</h2>

    <ul>
      <li v-for="product  in cart" :key="product.name">
       
       {{product.prix}} × {{product.quantity}} -> {{product.prix * product.quantity}} FCFA
      </li>
    </ul>

    <h3>Total : {{ total }} FCFA</h3>

    <p class="note">
      Le total se met à jour automatiquement.
    </p>
  </section>
</template>

<style scoped>
.card { padding:16px; border:1px solid #eee; border-radius:12px; }
.note { margin-top:8px; color:#555; }
</style>
<script setup>
import { ref } from "vue";

const products = ref([
  { id: 1, name: "lait", prix: 1000, quantity: 2 },
  { id: 2, name: "fromage", prix: 2000, quantity: 1 },
  { id: 3, name: "chocolat", prix: 1500, quantity: 3 },
]);
function removeProduct(id) {
  products.value = products.value.filter((p) => p.id !== id)
}
</script>

<template>
  <section class="card">
    <h2>13 - Lists</h2>

    <ul>
      <li v-for="p in products" :key="p.id">
        {{ p.name }} - {{ p.prix }} FCFA
        <button @click="removeProduct(p.id)">❌</button>
      </li>
    </ul>
  </section>
</template>

<style scoped>
.card { padding:16px; border:1px solid #eee; border-radius:12px; }
li { display:flex; justify-content:space-between; width:250px; }
button { border:none; background:none; cursor:pointer; }
</style>
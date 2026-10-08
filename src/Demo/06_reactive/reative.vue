    <script setup>
import { reactive, ref } from "vue";

const user = reactive({
  fullname: "Binetou Dia",
  phone: "772015403",
  solde: 3000,
});
function incrementSolde(amount) {
  user.solde += amount;
}
const cpt = ref(0);
const nombreajout = ref(0);
function incrementCpt(montant) {
  if (cpt.value < 10) {
    user.solde += montant;
    cpt.value++;
  }
  nombreajout.value = 0;
  return;
}
</script>

<template>
  <section class="card">
    <h2>09 - reactive()</h2>

    <div class="box">
      <p><strong>Nom :</strong> {{ user.fullname }}</p>
      <p><strong>Téléphone :</strong> {{ user.phone }}</p>
      <p><strong>Solde :</strong> {{ user.solde }} FCFA</p>
    </div>

    <div class="actions">
      <button @click="incrementSolde(5000)">+5 000</button>
      <button @click="incrementSolde(10000)">+10 000</button>
      <input
        type="number"
        v-model.number="nombreajout"
        placeholder="Montant à ajouter"
      />
      <button
        @click="incrementCpt(nombreajout)"
        @keyup.enter="incrementCpt(nombreajout)"
      >
        Ajouter
      </button>
    </div>

    <p class="note">
      <code>reactive()</code> est idéal pour les objets complexes.
    </p>
  </section>
</template>

<style scoped>
.card {
  padding: 16px;
  border: 1px solid #eee;
  border-radius: 12px;
}
.box {
  padding: 12px;
  background: #fafafa;
  border-radius: 10px;
}
.actions {
  display: flex;
  gap: 10px;
  margin-top: 10px;
}
button {
  padding: 8px 10px;
  border: 1px solid #ddd;
  border-radius: 8px;
}
.note {
  margin-top: 8px;
  color: #555;
}
</style>
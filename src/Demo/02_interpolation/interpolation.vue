<script setup>
const montant = 2000000;
const annee = new Date().getFullYear();
const prime=0.5;
const personne = {
    fullname: "BINETOU DIA",
    role: "developpeur", 
}
</script>

<template>
    <section class="card">
        <div class="div1"> MONTANT: {{ montant.toLocaleString() }}FCFA</div>
        <div class="div2">PRENOM: {{ personne.fullname }}</div>
        <div class="div3">ROLE: {{ personne.role }}</div>
       <div class="div4">ANNEE: {{ annee }}</div>
       <div class="div5">SALAIRE NET: {{ (montant + montant*prime).toLocaleString() }}FCFA</div>

    </section>
  
</template>


<style scoped>
.card{
  background:rgb(77, 138, 147);
  padding: 16px;
  border:1px solid #eee;
  border-radius:12px;
}

</style>
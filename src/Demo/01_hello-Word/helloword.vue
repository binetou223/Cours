<script setup>
const message = "BONJOUR TOUT LE MONDE";
</script>

<template>

  <section class="card">
    <H2>HELLO WORLD </H2>
    <P>Premier composant vue (SFC)</P>
    <div class="box">
        <strong>Message :</strong>{{message.toUpperCase()}}
    </div>
  </section>

</template>



<style  scoped>
.card{
  background:rgb(13, 91, 91);
  padding: 16px;
  border:1px solid #eee;
  border-radius:12px;
}
.box{
  margin-top: 10px ;
  padding: 12px;
  border: 1px dashed #ccc;
  border-radius:10px;

}
</style>
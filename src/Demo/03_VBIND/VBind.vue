<script setup>
const img="https://i.pinimg.com/originals/1b/f5/d6/1bf5d6a0ff5585770007b0c389223069.png";
const btn=false;
</script>


<template>
  <img :src="img" alt="">
 <button :disabled="btn">Valider</button>
</template>

<style>

</style>
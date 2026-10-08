<script setup>
import { ref } from "vue";
const step = ref(1);
const cpt=ref(0);
function Increment() {
    cpt.value+=step.value;
    
}
function Decrement() {
    cpt.value=0;
    
}
</script>

<template>
    <div>
        <div>
            <button @click="Increment">Increment +</button>
            <button @click="Decrement">Decrement</button>
        </div>
        <div>
         <input type="number" min="1" v-model.number="step" @keyup.enter="Increment">
        </div>
        <h4>{{ cpt }}</h4>
    </div>
  
</template>


<style>

</style>
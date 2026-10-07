<script setup>
import { ref } from "vue";
 const Status = ref('');
</script>

<template>
    <section class="card">
        <h2>04-Dynamic Attribut</h2>
        <div class="row">
            <span>Statut</span>
            <select v-model="Status">
                <option value="success">Success</option>
                <option value="warning">Warnig</option>
                <option value="danger">Danger</option>
            </select>
            <p>{{ Status }}</p>
        </div>
        <div class="bar" :style="{ width: '30%' }"></div>

    </section>
  
</template>



<style scoped>
.card{
  padding: 16px;
  border:1px solid #eee;
  border-radius:12px;
}
.row{
    display: flex;
    gap: 10px;
    align-items: center;
}
.badge{
    padding: 6px 12px;
    border-radius: 8px;
    font-weight: 600;
    border: 1px solid #eee;
}
.success{
    background: rgb(13, 91, 91);
}
.warning{
    background: rgb(255, 255, 0);
}
.danger{
    background: rgb(255, 0, 0);
}
.bar{
    height: 10px;
    background: rgb(13, 91, 91);
    margin-top: 14px;
    border: 1px solid #eee;
    border-radius: 8px;
}
select{
    padding: 6px 12px;
    border: 1px solid #ddd;
    border-radius: 8px;
}


</style>
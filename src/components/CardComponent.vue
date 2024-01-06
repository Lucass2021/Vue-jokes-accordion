<template>
    <div class="card-internal-container">
        <h1>Developers Joke</h1>
        <div class="accordion-list">
            <AccordionComponent/>
        </div>
    </div>
</template>

<script setup>
import AccordionComponent from './AccordionComponent.vue';


</script>

<style scoped>

.card-internal-container{
    background: #fff;
    padding:30px;
    width: 600px;
    margin:0 auto;
    border-radius:10px;
}

div h1{
    font-size: 40px;
    text-align: center;
    font-weight: 700;
}

</style>
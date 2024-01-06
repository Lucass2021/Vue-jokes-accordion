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
    padding:1.875rem;
    width: 37.5rem;
    margin:0 auto;
    border-radius:0.625rem;
}

div h1{
    font-size: 2.5rem;
    text-align: center;
    font-weight: 700;
}

@media only screen and (max-width: 767px) {
    .card-internal-container{
        width: 27.5rem;
    }
}
@media only screen and (max-width: 575px) {
    .card-internal-container{
        width: 22.5rem;
        padding: 1rem;
    }
}


</style>
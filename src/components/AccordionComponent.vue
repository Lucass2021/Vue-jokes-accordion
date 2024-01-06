<template>
    <div class="q-pa-md">
      <q-list bordered class="rounded-borders">
        <q-expansion-item expand-separator v-for="joke in jokeData" :key="joke.setup" :label="joke.setup" class="accordion-title">
            <q-card>
            <q-card-section>
                <p class="accordion-text">
                    {{ joke.delivery }}
                </p>
            </q-card-section>
          </q-card>
        </q-expansion-item>
      </q-list>
    </div>
</template>
  
<script setup>
    import { ref, onMounted } from "vue";

    let jokeData = ref([]);

    const handleJokeApiRequest = async () => {
        try {
            const req = await fetch(`https://v2.jokeapi.dev/joke/Programming?type=twopart&amount=5`);
            const json = await req.json();
            jokeData.value = json.jokes;
        } catch (error) {
            console.error("API ERROR", error);
        }
    };

    onMounted(() => {
        console.log("-Running API");
        handleJokeApiRequest();
        console.log(jokeData)
    });

</script>
  

<style scoped>

hr{
    color: #eee;
    opacity: 0.3;
}

.accordion-title{
    color: #301534;
    font-weight: 700;
}

.accordion-text{
    color: #686469;
    font-weight: 400;
    margin-bottom: 0px;
}


</style>
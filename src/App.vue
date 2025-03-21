<script setup>
import { ref } from 'vue'
import CardView from './components/CardView.vue';
import { userWatchList } from './assets/static/js/watchList.js';
const localSeries = ref(userWatchList);
</script>

<template>
    <div>
        <div class="container">
            <section class="sidebar">
                <ul>
                    <li>Ici c'est fixe</li>
                    <li>Un lien de nav 1</li>
                    <li>Un lien de nav 2</li>
                </ul>
                <span>▶ Lecture en cours: (ep title) </span>
            </section>
            <main class="courses-container">
                <!-- v-for permet de faire un element html par objet dans mon tableau d'objet -->
                <CardView v-for="serie in localSeries" :series="serie.series" :title="serie.title"
                    :episode="serie.episode" :season="serie.season" />
            </main>
        </div>
    </div>



</template>

<style scoped></style>

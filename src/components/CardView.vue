<script setup>
// je defini les proprietés de mon composant
const props = defineProps({
    series: String,
    season: Number,
    episode: Number,
    title: String,
    timeCursor: String,
})
</script>

<template>
    <!-- Dans mon template je place mon html et mes proprietés -->
    <div class="watch-card">
        <div class="course-preview">
            <h6>{{ series }}</h6>
            <h2>{{ title }}</h2>
        </div>
        <div class="course-info">
            <h6>Season{{ season }} x episode{{ episode }}</h6>
            <h2>{{ title }}</h2>
            <button class="btn">Continue</button>
        </div>
    </div>
</template>
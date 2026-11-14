<script setup>
    import { ref } from 'vue';
    import axios from 'axios';

    let searchQuery = ref("");
    async function fetchMovieByName(){
        const response = await axios.get(
            `https://api.themoviedb.org/3/search/movie?query=${searchQuery.value}`
        );

        const data = JSON.stringify(response.data);

        return data;
    } 
</script>
0
<style lang="css">
    .search-container {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 2px;
        gap: 8px
    }
    .search-bar {
        min-width: 100px;
        padding: 4px;
        border: none;
    }

    .search-button {
        padding: 4px;
        padding-inline: 24px;
        border-radius: 8px;
        border: none;
        background-color: white;

    }

    .filter-button {
        padding: 4px;
        padding-inline: 24px;
        border-radius: 8px;
        border: none;
        background-color: white;

    }
</style>

<template>
    <div class="search-container">
        <input 
            class="search-bar" 
            v-model="searchQuery"
            type="text"
            placeholder="Avengers Doomsday"
        />
        <button class="search-button" @click="fetchMovieByName">buscar</button>
        <button class="filter-button">filtrar</button>
    </div>
</template>
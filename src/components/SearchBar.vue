<script setup>

</script>

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
        <input class="search-bar" placeholder="Avengers Doomsday"/>
        <button class="search-button">buscar</button>
        <button class="filter-button">filtrar</button>
    </div>
</template>
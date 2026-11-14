<script setup>
    import './Header.css'
    import SearchBar from './SearchBar.vue';
</script>

<template>
    <div class="container">
        <h2 class="title">StoryTime</h2>
        <SearchBar/>
        <p>resultados para: {{ searchQuery }}</p>
    </div>
</template>
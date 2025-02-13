<template>
    <main class="home-container">
        <h1>Home Page</h1>
        <ButtonComponent :data="{id:'submit-btn', type:'submit', class:'bg-red-600 p-4 rounded-lg'}" />
        
    </main>
    </template>
    
    <script lang="ts" setup>

    import ButtonComponent from '../components/ButtonComponent.vue';

    </script>

    <style>
    </style>
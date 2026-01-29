<template>

<AppHeader />

 <div class="rental-block container">
        <!-- Основная информация -->
        <div class="rental-info">
            <p class="text-base"><a href="#">Посуточная аренда</a></p>
            <p class="text-base"><a href="#">Барановичи</a></p>
            <p class="text-base"><a href="#">70 - 150 BYN</a></p>
            <p class="text-base"><a href="#">27.09.25 - 30.09.25</a></p>
        </div> 
        
        <button class="save-button text-base">           
            Сохранить вариант
            <img src="./assets/like_grey.svg" 
                 alt=""
                 class="save-button__icon">
        </button>
    </div>
</template>

<script setup>
    import AppHeader from '@/components/layouts/AppHeader.vue'
</script>

<style>
    @import './assets/styles/globals.css';
</style>

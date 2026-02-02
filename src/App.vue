<template>
    <AppHeader />
    
    <div class="rental-block container">
      <!-- Основная информация -->
      <div class="rental-info">
        <p class="text-base">
          <a href="#">Посуточная аренда</a>
        </p>
        <p class="text-base">
          <a href="#">Барановичи</a>
        </p>
        <p class="text-base">
          <a href="#">70 - 150 BYN</a>
        </p>
        <p class="text-base">
          <a href="#">27.09.25 - 30.09.25</a>
        </p>
      </div>
      
      <button class="save-button text-base">
        Сохранить вариант
        <img
          src="./assets/icons/common/like-grey.svg"
          alt=""
          class="save-button__icon"
        >
      </button>
    </div>
  </template>
  
  <script setup>
  import AppHeader from '@/components/layouts/AppHeader.vue'
  </script>
  
  <style scoped>
  .rental-block {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    gap: 0.625rem;
    font-family: "Ubuntu", sans-serif;
    font-weight: 500;
    flex-wrap: wrap;
    padding: 1.375rem 0;
  }

  .rental-info {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;
    flex-wrap: wrap;
    flex: 1;
    gap: 0.875rem;
  }

  .rental-info p {
    transition: color 0.3s ease;
    white-space: nowrap;
  }

  .rental-info p::after {
    content: " /";
    margin-left: 0.375rem;
  }

  .rental-info p a{
    white-space: nowrap;
  }

  .rental-info p:last-child::after {
    content: "";
  }

  .rental-info p:hover {
    color: var(--primary);
  }

  .save-button {
    padding: 0.375rem 0.875rem;
    display: inline-flex;
    align-items: center;
    gap: 0.6rem;
    transition: color 0.3s ease;
  }

  .save-button:hover {
    color: var(--primary);
  }

  .save-button__icon {
    width: 1.5rem;
    height: 1.5rem;
  }

  @media (max-width: 925px) {
    .rental-block {
      flex-direction: column;
      align-items: stretch;
      gap: 1.5rem;
      padding: 1rem;
    }

    .rental-info p {
      gap: 0.375rem 0.875rem 0.375rem 0;
    }

    .save-button {
      align-self: flex-start;
      padding: 0.125rem 0;
    }
  }
  </style>
<template>
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
          src="@/assets/icons/common/like-grey.svg"
          alt=""
          class="save-button__icon"
        >
      </button>
    </div>
</template>

<script setup>

</script>

<style lang="scss">
$primary-color: var(--primary);
$font-family: "Ubuntu", sans-serif;
$font-weight: 500;
$breakpoint-tablet: 925px;
$breakpoint-mobile: 576px;

.rental-block {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  gap: 0.625rem;
  font-family: $font-family;
  font-weight: $font-weight;
  flex-wrap: wrap;
  padding: 1.375rem 0;

  .rental-info {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;
    flex-wrap: wrap;
    flex: 1;
    gap: 0.875rem;

    p {
      transition: color 0.3s ease;
      white-space: nowrap;
      position: relative;
      margin: 0;

      
      &::after {
        content: " /";
        margin-left: 0.375rem;
        color: inherit;
      }

      
      &:last-child::after {
        content: "";
        margin-left: 0;
      }

      a {
        white-space: nowrap;
        color: inherit;
        text-decoration: none;

        &:hover {
          color: $primary-color;
        }
      }

      
      &:hover {
        color: $primary-color;
        
        a {
          color: $primary-color;
        }
      }
    }
  }

  .save-button {
    padding: 0.375rem 0.875rem;
    display: inline-flex;
    align-items: center;
    gap: 0.6rem;
    transition: color 0.3s ease;
    background: none;
    border: none;
    cursor: pointer;
    font-family: inherit;
    font-weight: inherit;
    color: var(--grey-900);

    &:hover {
      color: $primary-color;
    }

    &__icon {
      width: 1.5rem;
      height: 1.5rem;
      transition: all 0.3s ease;
    }
  }


  @media (max-width: $breakpoint-tablet) {
    flex-direction: column;
    align-items: stretch;
    gap: 1.5rem;
    padding: 1rem;

    .rental-info {
      p {
        margin: 0 0.875rem 0.375rem 0;     
      }
    }

    .save-button {
      align-self: flex-start;
      padding: 0.125rem 0;
    }
  }

  @media (max-width: $breakpoint-mobile) {
    .rental-info {        
        align-items: flex-start;
        gap: 0rem 0.875rem;      
      p {
        margin: 0 0 0.375rem 0 !important;
      }
    }
    
    .save-button {
      width: 100%;
      justify-content: center;
      padding: 0.375rem 0.875rem;
    }
  }
}
</style>
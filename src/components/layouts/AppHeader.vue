<template>
  <header>
    <div class="container">
      <div class="logo_block">
        <img src="@/assets/logop.svg" alt="logo" />
      </div>

      <div class="menu_block">
        <div class="menu_block_left">
          <p class="text-base"><a href="#">Искать жильё</a></p>
          <p class="text-base"><a href="#">Блог</a></p>
          <p class="text-base"><a href="#">Частые вопросы</a></p>

          <img src="@/assets/zvon.svg" alt="" class="icon-svg" />
          <img src="@/assets/like.svg" alt="" class="icon-svg" />
        </div>

        <div class="menu_block_butt">
          <button class="my_account r8">
            Мой аккаунт
          </button>
        </div>
      </div>

      <!-- Бургер -->
      <button class="burger-btn r6" aria-label="Открыть меню">
        <div class="burger-icon">
          <div class="burger-line line1 r6"></div>
          <div class="burger-line line2 r6"></div>
          <div class="burger-line line3 r6"></div>
        </div>
      </button>
    </div>
  </header>
</template>

<script setup>

</script>

<style scoped>
header{
    padding:1rem 1.5rem;
    font-family: "Ubuntu", sans-serif;
    border-bottom: 1px solid #E5E5E7;
   
}
header .container{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
}
.my_account{
    font-size: 1rem; 
    line-height: 1.5; 
    color: var(--black);
    border: 1px solid var(--black);
    padding: 0.8rem 1.5rem;
    font-weight: 500;
    transition: color 0.3s ease, border-color 0.3s ease;
}
.my_account:hover{
    border-color: var(--primary);
    color: var(--primary);
   
}
.menu_block{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    gap: 1.5rem;
}
.menu_block_left{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    gap: 1rem;
}
.menu_block_left p a{
    padding: 0.375rem 0.875rem;
    transition: color 0.3s ease;
    font-weight: 500;
}
.menu_block_left p a:hover{
    color: var(--primary);
}
/* .icon-svg {
    transition: filter 0.3s ease;
}
.icon-svg:hover {
    filter: brightness(0) saturate(100%) 
            invert(32%) sepia(98%) saturate(1658%) 
            hue-rotate(204deg) brightness(102%) contrast(95%);
    
} */

/* Бургер-кнопка */
.burger-btn {
    display: none;
    background: none;
    border: none;
    cursor: pointer;
    width: 52px;
    height: 52px;
    position: relative;
    padding: 0;
    z-index: 100;
    justify-content: center;
    align-items: center;
    border: 1px solid var(--black);

}

.burger-icon {
    position: relative;
    width: 16px;
    height: 12px;
}

.burger-line {
    position: absolute;
    background-color: #000;
    height: 2px;
    left: 0;
    transition: all 0.3s ease;
}
.line1 {
    top: 0;
    width: 1rem;
}

.line2 {
    top: 0.25rem;
    width: 1rem; 
}

.line3 {
    top: 0.5rem;
    width: 1rem;
}
</style>
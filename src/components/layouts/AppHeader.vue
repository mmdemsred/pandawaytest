<template>
  <header class="header">
    <div class="container">
      <div class="logo-block">
        <img src="@/assets/icons/common/logop.svg" alt="Логотип" />
      </div>

      <div class="menu-block">
        <div class="menu-block-left">
          <p class="text-base">
            <a href="#">Искать жильё</a>
          </p>
          <p class="text-base">
            <a href="#">Блог</a>
          </p>
          <p class="text-base">
            <a href="#">Частые вопросы</a>
          </p>

          <img
            src="@/assets/icons/common/zvon.svg"
            alt="Уведомления"
            class="icon-svg"
          />
          <img
            src="@/assets/icons/common/like.svg"
            alt="Избранное"
            class="icon-svg"
          />
        </div>

        <div class="menu-block-button">
          <button class="account-btn r8">
            Мой аккаунт
          </button>
        </div>
      </div>

      <!-- Бургер меню -->
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
// Компонент не требует логики
</script>

<style lang="scss" scoped>
.header {
  padding: 1rem 1.5rem;
  font-family: "Ubuntu", sans-serif;
  border-bottom: 1px solid #e5e5e7;

  .container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
  }

  .menu-block {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    gap: 1.5rem;

    &-left {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: space-between;
      gap: 1rem;

      p {
        a {
          padding: 0.375rem 0.875rem;
          transition: color 0.3s ease;
          font-weight: 500;
          white-space: nowrap;

          &:hover {
            color: var(--primary);
          }
        }
      }
    }

    &-button {
      .account-btn {
        font-size: 1rem;
        line-height: 1.5;
        color: var(--black);
        border: 1px solid var(--black);
        padding: 0.8rem 1.5rem;
        font-weight: 500;
        transition: color 0.3s ease, border-color 0.3s ease;
        background: none;
        cursor: pointer;

        &:hover {
          border-color: var(--primary);
          color: var(--primary);
        }
      }
    }
  }

  .icon-svg {
    cursor: pointer;
    transition: opacity 0.3s ease;

    &:hover {
      opacity: 0.8;
    }
  }

  /* Бургер-кнопка */
  .burger-btn {
    display: none;
    background: none;
    border: none;
    cursor: pointer;
    width: 3.25rem;
    height: 3.25rem;
    position: relative;
    padding: 0;
    z-index: 100;
    justify-content: center;
    align-items: center;
    border: 1px solid var(--black);

    .burger-icon {
      position: relative;
      width: 1rem;
      height: 0.75rem;

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
    }
  }

  /* Адаптивность */
  @media (max-width: 1024px) {
    .menu-block {
      gap: 1rem;

      &-left {
        gap: 0.75rem;
      }
    }
  }

  @media (max-width: 925px) {
    .menu-block {
      display: none;
    }

    .burger-btn {
      display: flex;
    }
    .header {
      padding: 1rem;
    }
  }

  @media (max-width: 399px) {
    .logo-block {
      max-width: 160px;
    }
  }
}
</style>
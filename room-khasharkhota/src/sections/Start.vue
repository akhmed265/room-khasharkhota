<template>
  <section class="start">
    <div class="container">
      <header class="header">
        <a href="" class="header__logo">
          <img src="../assets/image/logo.svg" alt="Logo" />
        </a>
        <nav class="header__nav">
          <ul class="nav__list">
            <li class="nav__item">
              <a href="" class="nav__link"> Главная </a>
            </li>
            <li class="nav__item">
              <a href="" class="nav__link"> Про гида </a>
            </li>
            <li class="nav__item">
              <a href="" class="nav__link"> Программа тура </a>
            </li>
            <li class="nav__item">
              <a href="" class="nav__link"> Стоимость </a>
            </li>
            <li class="nav__item">
              <a href="" class="nav__link"> Блог </a>
            </li>
            <li class="nav__item">
              <a href="" class="nav__link"> Контакты </a>
            </li>
          </ul>
        </nav>
        <Button variant="dark-to-light" type?="button">
          Консультация
        </Button>
      </header>

      <div class="start__info">
        <h1 class="start__title">
          Насладись прогулкой в горах с командой единомышленников
        </h1>
        <from class="start__search">
          
        </from>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import Button from '@/components/UI/Button.vue'
</script>

<style scoped lang="scss">
@import "../styles/variables.scss";

.start {
  background-image: url(@/assets/image/banner.jpg);
  background-size: cover;
  background-position: center;
  font-family: $font-nunito;

  .container {
    padding-right: 370px;
    padding-left: 370px;
  }

  .header {
    display: flex;
    align-items: center;
    padding-top: 16px;

    .nav__list {
      display: flex;
      align-items: center;
      gap: 24px;
      list-style: none;
      margin-left: 212px;
      margin-right: 49px;
    }

    .nav__link {
      font-size: $font-nav;
      color: $secondary-color;
      font-weight: 600;
      text-decoration: none;

      &:hover {
        color: $yellow-color;
      }
    }
  }
}
</style>

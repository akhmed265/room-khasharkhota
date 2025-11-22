<template>
  <section class="start">
    <div class="container">
      <header class="header">
        <a href="" class="header__logo">
          <img
            src="../assets/image/logo.svg"
            alt="Logo"
            class="header__logo-img"
          />
        </a>

        <button
          class="burger"
          :class="{ 'burger--active': isMenuOpen }"
          @click="toggleMenu"
        >
          <img src="@/assets/icons/burger.svg" alt="бургер" />
        </button>

        <nav class="header__nav" :class="{ 'header__nav--active': isMenuOpen }">
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

          <button class="close" @click="toggleMenu">
            <img src="@/assets/icons/close.svg" alt="закрыть" />
          </button>
        </nav>
        <Button variant="dark-to-light" type="button" class="header__btn">
          Консультация
        </Button>
      </header>

      <div class="start__info">
        <h1 class="start__title">
          Насладись прогулкой в горах с&nbsp;командой единомышленников
        </h1>

        <from class="start__search">
          <div class="start__label">
            <select
              v-model="form.location"
              class="start__location"
              name="location"
              required
            >
              <option value="" disabled class="option-title">
                Локация для тура
              </option>
              <option value="uk">Великобритания</option>
              <option value="ru">Россия</option>
              <option value="us">США</option>
            </select>
            <span class="start__span">выберите из списка</span>
          </div>

          <div class="start__label">
            <div class="start__block-date">
              <input
                v-model="form.startDate"
                class="start__date"
                type="date"
                name="start-date"
                placeholder="Начало"
                required
              />
              <input
                v-model="form.endDate"
                class="start__date"
                type="date"
                name="final-date"
                placeholder="Конец"
                required
              />
            </div>
            <span class="start__span">укажите диапазон</span>
          </div>

          <div class="start__label">
            <select
              v-model="form.quantity"
              class="start__quantity"
              name="quantity"
              required
            >
              <option value="" disabled class="option-title">Участники</option>
              <option value="4">4</option>
              <option value="5">5</option>
              <option value="6">6</option>
            </select>
            <span class="start__span">минимум 4 человека</span>
          </div>
          <Button variant="light-to-dark" type="button" class="search__btn">
            Найти программу
          </Button>
        </from>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import Button from "@/components/UI/Button.vue";

import { ref } from "vue";

interface SearchForm {
  location: string;
  startDate: string;
  endDate: string;
  quantity: string;
}

const form = ref<SearchForm>({
  location: "",
  startDate: "",
  endDate: "",
  quantity: "",
});

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
  if (isMenuOpen.value) {
    document.body.style.overflow = "hidden";
  } else {
    document.body.style.overflow = "";
  }
};

const handleSubmit = () => {
  console.log("Данные формы:", form.value);
};
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

    @media (max-width: 1100px) {
      padding-left: 10px;
      padding-right: 10px;
    }
  }

  .header {
    display: flex;
    align-items: center;
    padding-top: 16px;
    position: relative;

    .header__nav {
      .nav__list {
        display: flex;
        align-items: center;
        gap: 24px;
        list-style: none;
        margin-left: 193px;
        margin-right: 35px;

        @media (max-width: 1100px) {
          align-items: flex-start;
          flex-direction: column;
          margin: 0;
          gap: 24px;
        }
      }

      .nav__link {
        font-size: $font-nav;
        color: $secondary-color;
        font-weight: 600;
        text-decoration: none;
        white-space: nowrap;

        &:hover {
          color: $yellow-color;
        }
      }

      .close {
        display: none;
        position: absolute;
        top: 45px;
        right: 10px;
        background-color: transparent;
        border: none;
        cursor: pointer;
        padding: 0;
        z-index: 10;

        @media (max-width: 1100px) {
          display: block;
        }
      }

      @media (max-width: 1100px) {
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        background-color: $green-color;
        backdrop-filter: blur(100px);
        transform: translateX(-150%);
        opacity: 0;
        visibility: hidden;
        transition: all 0.3s ease;
        z-index: 5;
        width: 100%;
        height: 100%;
        padding: 45px 16px 50px;

        &--active {
          transform: translateX(0);
          opacity: 1;
          visibility: visible;
        }
      }
    }

    .burger {
      display: none;
      background: transparent;
      border: none;
      cursor: pointer;
      padding: 0;
      z-index: 1000;

      @media (max-width: 1100px) {
        display: flex;
      }

      &--active {
        display: none;
      }
    }

    &__btn {
      @media (max-width: 1100px) {
        display: none;
      }
    }

    @media (max-width: 1100px) {
      justify-content: space-between;
    }
  }

  &__info {
    padding-top: 416px;
    padding-bottom: 82px;

    .start__title {
      font-family: $font-custom;
      font-size: 50px;
      color: $secondary-color;
      margin-bottom: 41px;
    }

    .start__search {
      display: flex;
      background-color: rgba(255, 255, 255, 0.2);
      backdrop-filter: blur(6px);
      padding: 40px 42px;
      gap: 24px;
      border-radius: 10px;

      .start__label {
        display: flex;
        flex-direction: column;

        .start__location,
        .start__quantity {
          position: relative;
          padding: 14px 16px;
          border: 1px solid #ddd;
          border-radius: 8px;
          font-family: inherit;
          font-size: 16px;
          background: transparent;
          color: $secondary-color;
          min-width: 270px;
          appearance: none;

          &:focus {
            outline: none;
            border-color: #1a3e3e;
          }

          option {
            background-color: $green-color;
            color: $secondary-color;
          }

          option:hover {
            background-color: $secondary-color;
            color: $green-color;
          }

          @media (max-width: 1100px) {
            min-width: 234px;
          }
        }
      }

      .start__block-date {
        display: flex;
        align-items: center;
        gap: 8px;

        .start__date {
          padding: 0 8px;
          border: 1px solid $secondary-color;
          border-radius: 8px;
          background-color: transparent;
          color: $secondary-color;
          font-family: inherit;
          height: 52px;

          &:focus {
            outline: none;
            border-color: #1a3e3e;
          }
        }

        .start__date::-webkit-calendar-picker-indicator {
          filter: invert(98%); /* Для #FDFDFD */
        }
      }

      .search__btn {
        width: 100%;
        height: 52px;
        padding: 15px;

        @media (max-width: 1100px) {
          height: 47px;
          padding: 15px;
        }
      }

      .start__span {
        color: $secondary-color;
        font-size: $font-small;
        font-weight: 400;
        margin-top: 8px;
      }
    }
  }
}
</style>

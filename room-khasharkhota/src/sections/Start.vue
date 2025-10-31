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
        <Button variant="dark-to-light" type="button"> Консультация </Button>
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

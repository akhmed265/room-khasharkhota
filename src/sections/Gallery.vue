<template>
  <section class="gallery">
    <div class="container">
      <div class="gallery__content">
        <p class="gallery__subtitle subtitle">фото-отчет</p>
        <h2 class="gallery__title title">Делимся впечатлениями</h2>
      </div>

      <ul class="gallery__list">
        <li class="gallery__item">
          <img
            src="@/assets/image/gallery.jpg"
            alt="Фотосессия в горах"
            class="gallery__img"
          />
          <button class="gallery__pic-overlay"></button>
        </li>
        <li class="gallery__item">
          <img
            src="@/assets/image/gallery-2.jpg"
            alt="Карта"
            class="gallery__img"
          />
          <button class="gallery__pic-overlay"></button>
        </li>
        <li class="gallery__item">
          <img
            src="@/assets/image/gallery-3.jpg"
            alt="Дубай"
            class="gallery__img"
          />
          <button class="gallery__pic-overlay"></button>
        </li>
        <li class="gallery__item">
          <img
            src="@/assets/image/gallery-4.jpg"
            alt="Пляж с высоты"
            class="gallery__img"
          />
          <button class="gallery__pic-overlay"></button>
        </li>
        <li class="gallery__item">
          <img
            src="@/assets/image/gallery-5.jpg"
            alt="Горы"
            class="gallery__img"
          />
          <button class="gallery__pic-overlay"></button>
        </li>
        <li class="gallery__item">
          <img
            src="@/assets/image/gallery-6.jpg"
            alt="Карта"
            class="gallery__img"
          />
          <button class="gallery__pic-overlay"></button>
        </li>
      </ul>

      <Button variant="dark-to-light" type="button" class="gallery__btn">
        Наш pinterest
      </Button>
    </div>
  </section>
</template>

<script setup lang="ts">
import Button from "@/components/UI/Button.vue";
</script>

<style scoped lang="scss">
@import "../styles/variables.scss";

.gallery {
  font-family: $font-nunito;

  .container {
    padding-top: 80px;
    padding-bottom: 100px;
    padding-left: 370px;
    padding-right: 370px;
    text-align: center;

    .gallery__list {
      display: grid;
      grid-template-columns: repeat(12, 1fr);
      grid-auto-rows: 250px;
      margin-bottom: 50px;
      gap: 20px;
      list-style: none;
      justify-content: center;

      .gallery__item {
        position: relative;
        border-radius: 6px;
        overflow: hidden;
        height: 250px;

        &:nth-child(1) {
          grid-column: span 6;
          grid-row: 1;
        }
        &:nth-child(2) {
          grid-column: span 3;
          grid-row: 1;
        }
        &:nth-child(3) {
          grid-column: span 3;
          grid-row: 1;
        }

        // Второй ряд: кастомное расположение
        &:nth-child(4) {
          grid-column: span 3;
          grid-row: 2;
        }
        &:nth-child(5) {
          grid-column: span 6; // Занимает две колонки
          grid-row: 2;
        }
        &:nth-child(6) {
          grid-column: span 3;
          grid-row: 2;
        }

        .gallery__img {
          width: 100%;
          height: 100%;
          object-fit: cover;
          display: block;
        }

        .gallery__pic-overlay {
          position: absolute;
          inset: 0;
          display: flex;
          align-items: center;
          justify-content: center;
          border: 0;
          padding: 0;
          background-color: rgba(26, 62, 62, 0);
          background-image: url(../assets/icons/loupe.svg);
          background-repeat: no-repeat;
          background-position: center;
          opacity: 0;
          transition: all 0.3s;
          cursor: pointer;

          &:hover {
            background-color: rgba(26, 62, 62, 0.3);
            opacity: 1;
          }
        }
      }
    }

    @media (max-width: 1100px) {
      padding-left: 10px;
      padding-right: 10px;
    }
  }
}
</style>

<template>
  <section class="blog">
    <div class="container">
      <blog__content>
        <p class="blog__subtitle subtitle">делимся впечатлениями</p>
        <h2 class="blog__title title">Блог о путешествиях</h2>
      </blog__content>

      <ul class="news__list">
        <li class="news__item">
          <img
            src="@/assets/image/blog.jpg"
            alt="Итальянский город"
            class="news__img"
          />
          <div class="news__content">
            <a href="#" class="news__title-link"
              >Красивая Италя, какая <br />
              она&nbsp;в реальности?</a
            >
            <p class="news__descr">
              Для современного мира базовый вектор развития&nbsp;предполагает
              независимые способы&nbsp;реализации соответствующих
              условий&nbsp;активизации.
            </p>
            <div class="news__info">
              <time datetime="01/04/2023" class="news__time">01/04/2023</time>
              <a href="#" class="news__link">читать статью</a>
            </div>
          </div>
        </li>
        <li class="news__item">
          <img
            src="@/assets/image/blog-2.jpg"
            alt="Вид на небо из самолета"
            class="news__img"
          />
          <div class="news__content">
            <a href="#" class="news__title-link"
              >Долой сомнения! Весь мир&nbsp;открыт для вас!</a
            >
            <p class="news__descr">
              Для современного мира базовый вектор развития&nbsp;предполагает
              независимые способы&nbsp;реализации соответствующих
              условий&nbsp;активизации
            </p>
            <div class="news__info">
              <time datetime="01/04/2023" class="news__time">01/04/2023</time>
              <a href="#" class="news__link">читать статью</a>
            </div>
          </div>
        </li>
        <li class="news__item">
          <img
            src="@/assets/image/blog-3.jpg"
            alt="Девушка в узкой улице"
            class="news__img"
          />
          <div class="news__content">
            <a href="#" class="news__title-link"
              >Как подготовиться к&nbsp;путешествию в&nbsp;одиночку?</a
            >
            <p class="news__descr">
              Для современного мира базовый вектор развития предполагает.
            </p>
            <div class="news__info">
              <time datetime="01/04/2023" class="news__time">01/04/2023</time>
              <a href="#" class="news__link">читать статью</a>
            </div>
          </div>
        </li>
        <li class="news__item">
          <img
            src="@/assets/image/blog-4.jpg"
            alt="Индийский храм"
            class="news__img"
          />
          <div class="news__content">
            <a href="#" class="news__title-link">Индия… летим?</a>
            <p class="news__descr">Для современного мира базовый.</p>
            <div class="news__info">
              <time datetime="01/04/2023" class="news__time">01/04/2023</time>
              <a href="#" class="news__link">читать статью</a>
            </div>
          </div>
        </li>
      </ul>
      <Button variant="dark-to-light" type="button" class="blog__btn">
        Рейтинг направлений
      </Button>
    </div>
  </section>
</template>

<script setup lang="ts">
import Button from "@/components/UI/Button.vue";
</script>

<style lang="scss">
@import "../styles/variables.scss";

.blog {
  font-family: $font-nunito;
  background-color: $background-color;

  .container {
    padding-top: 80px;
    padding-bottom: 100px;
    padding-left: 370px;
    padding-right: 370px;
    text-align: center;

    .news__list {
      display: grid;
      grid-template-columns: repeat(2, 580px);
      column-gap: 20px;
      row-gap: 24px;
      margin-bottom: 50px;
      list-style: none;

      @media (max-width: 1100px) {
        grid-template-columns: repeat(2, 530px);
        gap: 20px;
      }
    }

    .news__item {
      display: flex;
      padding: 16px;
      background-color: $secondary-color;
      border-radius: 10px;
      gap: 24px;

      .news__img {
        min-width: 230px;
        max-width: 230px;
        height: 280px;
        border-radius: 6px;
        object-fit: cover;

        @media (max-width: 1100px) {
          width: 220px;
          height: 290px;
        }
      }

      .news__content {
        text-align: left;
        padding-top: 16px;
        margin-bottom: 24px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        flex-grow: 1;

        .news__title-link {
          font-size: $font-medium;
          color: $text-color;
          font-weight: 700;
          line-height: 32px;
          text-decoration: none;
          transition: all 0.1s;
          cursor: pointer;

          &:hover {
            color: $green-color;
            text-decoration: underline 1px solid $green-color;
          }
        }

        .news__descr {
          font-size: $font-small;
          color: $text-color;
          font-weight: 400;
          line-height: 20px;
          margin-bottom: 24px;
        }

        .news__info {
          display: flex;
          align-items: center;
          justify-content: space-between;

          .news__time {
            font-size: $font-small;
            color: $yellow-color;
            font-weight: 700;
          }

          .news__link {
            font-size: $font-small;
            color: $green-color;
            font-weight: 700;
            text-decoration: none;
            transition: all 0.1s;
            cursor: pointer;

            &:hover {
              text-decoration: underline 1px solid $green-color;
            }
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

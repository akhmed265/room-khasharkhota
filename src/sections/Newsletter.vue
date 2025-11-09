<template>
  <section class="newsletter">
    <div class="container">
      <div class="newsletter__wrapper">
        <div class="newsletter__content">
          <p class="newsletter__subtitle subtitle">актуально</p>
          <h2 class="newsletter__title title">
            Получайте полезные рассылки о путешествиях
          </h2>
        </div>
        <div class="newsletter__subscribe">
          <p class="newsletter__text">Введите e-mail адрес</p>
          <form action="" class="newsletter__form">
            <label for="" class="newsletter__label">
              <input
                type="email"
                class="newsletter__input"
                inputmode="email"
                name="email"
                placeholder="name@domain.com"
                required="required"
              />
            </label>
            <Button
              variant="dark-to-light"
              type="button"
              class="newsletter__btn"
            >
              Подписаться на новости
            </Button>
          </form>
          <p class="newsletter__terms">
            подписываясь на&nbsp;новости, вы&nbsp;автоматически соглашаетесь
            с&nbsp;
            <a class="newsletter__terms-link" href="#">
              условиями обработки&nbsp;персональных данных</a
            >
            и&nbsp;
            <a class="newsletter__terms-link" href="#">
              правилами рекламных рассылок
            </a>
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import Button from "@/components/UI/Button.vue";
</script>

<style scoped lang="scss">
@import "../styles/variables.scss";

.newsletter {
  font-family: $font-nunito;

  .container {
    padding: 0 370px;

    .newsletter__wrapper {
      position: relative;
      z-index: 1;
      display: flex;
      justify-content: space-between;
      background-color: $secondary-color;
      box-shadow: 0 0 15px 0 rgba(24, 18, 30, 0.12);
      border-radius: 6px;
      padding: 40px 100px;
      gap: 64px;

      .newsletter__content {
        .newsletter__subtitle {
          font-size: $font-nav;
        }

        .newsletter__title {
          font-size: 26px;
          font-weight: 120%;
          margin: 0;
        }
      }

      .newsletter__subscribe {
        .newsletter__text {
          font-size: $font-input;
          color: $text-color;
          font-weight: 600;
          margin-bottom: 8px;
        }

        .newsletter__input {
          font-size: $font-small;
          color: $text-color;
          font-weight: 300;
          border-radius: 4px;
          border: none;
          background-color: $background-color;
          width: 280px;
          margin-right: 16px;
          padding: 12px 16px;
        }

        .newsletter__btn {
          padding: 11px 24px;
        }

        .newsletter__terms {
          font-size: $font-small;
          color: $text-color;
          font-weight: 600;
          line-height: 18px;
          margin-top: 8px;

          &-link {
            color: $text-color;
          }
        }
      }
    }
  }
}
</style>

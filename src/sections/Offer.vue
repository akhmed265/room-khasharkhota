<template>
  <section class="offer">
    <div class="container">
      <div class="offer__wrapper">
        <div class="offer__content">
          <p class="offer__subtitle subtitle">наше предложение</p>
          <h2 class="offer__title title">Лучшие программы для тебя</h2>
          <p class="offer__text text">
            Его корни уходят в один фрагмент классической латыни 45 года
            н.э.,&nbsp;то&nbsp;есть более двух тысячелетий назад. Ричард
            МакКлинток, профессор латыни из колледжа.
          </p>

          <ul class="offer__list">
            <li class="offer__item">
              <img
                src="@/assets/icons/offer-icon.svg"
                alt=""
                class="offer__item-img"
              />
              <div class="offer__item-content">
                <span class="offer__item-title">Опытный гид</span>
                <p class="offer__item-text">
                  Для современного мира базовый вектор развития предполагает
                  независимые способы реализации соответствующих условий
                  активизации.
                </p>
              </div>
            </li>
            <li class="offer__item">
              <img
                src="@/assets/icons/offer-icon-2.svg"
                alt=""
                class="offer__item-img"
              />
              <div class="offer__item-content">
                <span class="offer__item-title">Безопасный поход</span>
                <p class="offer__item-text">
                  Для современного мира базовый вектор развития предполагает
                  независимые способы реализации соответствующих условий
                  активизации.
                </p>
              </div>
            </li>
            <li class="offer__item">
              <img
                src="@/assets/icons/offer-icon-3.svg"
                alt=""
                class="offer__item-img"
              />
              <div class="offer__item-content">
                <span class="offer__item-title">Лояльные цены</span>
                <p class="offer__item-text">
                  Для современного мира базовый вектор развития предполагает
                  независимые способы реализации соответствующих условий
                  активизации.
                </p>
              </div>
            </li>
          </ul>

          <Button variant="dark-to-light" type="button">
            Стоимость программ
          </Button>
        </div>

        <div class="offer__media">
          <img src="@/assets/image/offer.png" alt="" class="offer__img" />
          <img src="@/assets/image/offer-2.png" alt="" class="offer__img" />
          <img src="@/assets/image/offer-3.png" alt="" class="offer__img" />
          <img src="@/assets/image/offer-4.png" alt="" class="offer__img" />
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
.offer {
  font-family: $font-nunito;
  .container {
    padding-top: 80px;
    padding-bottom: 100px;
    padding-left: 370px;
    padding-right: 370px;
    background-color: $background-color;
    .offer__wrapper {
      display: flex;
      justify-content: space-between;

      .offer__content {
        margin-right: 90px;

        .offer__list {
          list-style: none;

          .offer__item {
            display: flex;
            align-items: center;
            margin-bottom: 40px;

            &-img {
              margin-right: 16px;
              padding: 7px;
              border-radius: 4px;
            }

            &-title {
              font-size: $font-nav;
              color: $text-color;
              font-weight: 700;
              margin-bottom: 4px;
            }

            &-text {
              font-size: $font-small;
              color: $black-color;
              line-height: 20px;
            }
          }
        }
      }
      .offer__media {
          display: grid;
          grid-template-columns: repeat(2, 250px);
          align-content: center;
          gap: 10px;

          .offer__img {
            height: 250px;
            width: 250px;
          }
        }
    }
  }
}
</style>

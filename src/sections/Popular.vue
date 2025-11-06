<template>
  <section class="popular">
    <div class="container">
      <div class="popular__content">
        <p class="popular__subtitle subtitle">по версии отдыхающих</p>
        <h2 class="popular__title title">Популярные направления</h2>
      </div>

      <div class="popular__media swiper">
        <div class="popular__item">
          <img
            src="@/assets/image/popular.png"
            alt="Озеро возле гор"
            class="popular__img"
          />
          <div class="popular__rating">
            <svg width="18" height="17" viewBox="0 0 18 17" fill="none">
              <path
                d="M8.55696 13.6975L12.707 16.2075C13.467 16.6675 14.397 15.9875 14.197 15.1275L13.097 10.4075L16.767 7.2275C17.437 6.6475 17.077 5.5475 16.197 5.4775L11.367 5.0675L9.47696 0.6075C9.13696 -0.2025 7.97696 -0.2025 7.63696 0.6075L5.74696 5.0575L0.916957 5.4675C0.0369575 5.5375 -0.323043 6.6375 0.346957 7.2175L4.01696 10.3975L2.91696 15.1175C2.71696 15.9775 3.64696 16.6575 4.40696 16.1975L8.55696 13.6975Z"
                fill="#F2BE22"
              />
            </svg>
            4.9
          </div>

          <div class="popular__overlay overlay">
            <div class="overlay__info">
              <div class="overlay__title">
                <span class="overlay__name">Озеро возле гор</span>
                <p class="overlay__name-descr">романтическое приключение</p>
              </div>
              <span class="overlay__price"> 480 $ </span>
            </div>

            <p class="overlay__descr">
              Его корни уходят в&nbsp;один фрагмент классической латыни 45 года
              н.&nbsp;э., то&nbsp;есть более двух тысячелетий назад. Ричард
              МакКлинток, профессор латыни из&nbsp;колледжа Hampden-Sydney, штат
              Вирджиния, взял одно из&nbsp;самых странных слов в&nbsp;Lorem
              Ipsum, «consectetur» и&nbsp;занялся его поисками
              в&nbsp;классической латинской литературе.
            </p>

            <Button variant="dark-to-light" type="button" class="overlay__btn">
              Программа тура
            </Button>
          </div>
        </div>

        <div class="popular__item">
          <img
            src="@/assets/image/popular-2.png"
            alt="Ночь в горах"
            class="popular__img"
          />
          <div class="popular__rating">
            <svg width="18" height="17" viewBox="0 0 18 17" fill="none">
              <path
                d="M8.55696 13.6975L12.707 16.2075C13.467 16.6675 14.397 15.9875 14.197 15.1275L13.097 10.4075L16.767 7.2275C17.437 6.6475 17.077 5.5475 16.197 5.4775L11.367 5.0675L9.47696 0.6075C9.13696 -0.2025 7.97696 -0.2025 7.63696 0.6075L5.74696 5.0575L0.916957 5.4675C0.0369575 5.5375 -0.323043 6.6375 0.346957 7.2175L4.01696 10.3975L2.91696 15.1175C2.71696 15.9775 3.64696 16.6575 4.40696 16.1975L8.55696 13.6975Z"
                fill="#F2BE22"
              />
            </svg>
            4.5
          </div>

          <div class="popular__overlay overlay">
            <div class="overlay__info">
              <div class="overlay__title">
                <span class="overlay__name">Ночь в горах</span>
                <p class="overlay__name-descr">в компании друзей</p>
              </div>
              <span class="overlay__price"> 500 $ </span>
            </div>

            <p class="overlay__descr">
              Его корни уходят в&nbsp;один фрагмент классической латыни 45 года
              н.&nbsp;э., то&nbsp;есть более двух тысячелетий назад. Ричард
              МакКлинток, профессор латыни из&nbsp;колледжа Hampden-Sydney, штат
              Вирджиния, взял одно из&nbsp;самых странных слов в&nbsp;Lorem
              Ipsum, «consectetur» и&nbsp;занялся его поисками
              в&nbsp;классической латинской литературе.
            </p>

            <Button variant="dark-to-light" type="button" class="overlay__btn">
              Программа тура
            </Button>
          </div>
        </div>

        <div class="popular__item">
          <img
            src="@/assets/image/popular-3.png"
            alt="Йога в горах"
            class="popular__img"
          />

          <div class="popular__rating">
            <svg width="18" height="17" viewBox="0 0 18 17" fill="none">
              <path
                d="M8.55696 13.6975L12.707 16.2075C13.467 16.6675 14.397 15.9875 14.197 15.1275L13.097 10.4075L16.767 7.2275C17.437 6.6475 17.077 5.5475 16.197 5.4775L11.367 5.0675L9.47696 0.6075C9.13696 -0.2025 7.97696 -0.2025 7.63696 0.6075L5.74696 5.0575L0.916957 5.4675C0.0369575 5.5375 -0.323043 6.6375 0.346957 7.2175L4.01696 10.3975L2.91696 15.1175C2.71696 15.9775 3.64696 16.6575 4.40696 16.1975L8.55696 13.6975Z"
                fill="#F2BE22"
              />
            </svg>
            5.0
          </div>

          <div class="popular__overlay overlay">
            <div class="overlay__info">
              <div class="overlay__title">
                <span class="overlay__name">Йога в горах</span>
                <p class="overlay__name-descr">
                  для тех, кто забоится о&nbsp;себе
                </p>
              </div>
              <span class="overlay__price"> 230 $ </span>
            </div>

            <p class="overlay__descr">
              Его корни уходят в&nbsp;один фрагмент классической латыни 45 года
              н.&nbsp;э., то&nbsp;есть более двух тысячелетий назад. Ричард
              МакКлинток, профессор латыни из&nbsp;колледжа Hampden-Sydney, штат
              Вирджиния, взял одно из&nbsp;самых странных слов в&nbsp;Lorem
              Ipsum, «consectetur» и&nbsp;занялся его поисками
              в&nbsp;классической латинской литературе.
            </p>

            <Button variant="dark-to-light" type="button" class="overlay__btn">
              Программа тура
            </Button>
          </div>
        </div>
      </div>

      <Button variant="dark-to-light" type="button" class="popular__btn">
        Рейтинг направлений
      </Button>
    </div>
  </section>
</template>

<script setup lang="ts">
import Button from "@/components/UI/Button.vue";
</script>

<style scoped lang="scss">
@import "../styles/variables.scss";

.popular {
  font-family: $font-nunito;

  .container {
    padding-top: 80px;
    padding-bottom: 100px;
    padding-left: 370px;
    padding-right: 370px;
    text-align: center;

    .popular__content {
      text-align: center;
    }

    .popular__media {
      display: flex;
      justify-content: space-between;
      margin-bottom: 50px;

      .popular__item {
        position: relative;
        width: 380;
        height: 500;
        border-radius: 32px;
        overflow: hidden;

        &:hover .overlay {
          top: 0;
        }

        .popular__rating {
          position: absolute;
          display: flex;
          align-items: center;
          gap: 4px;
          top: 50px;
          right: 0;
          width: 65;
          height: 32;
          padding: 4px 8px;
          border-top-left-radius: 4px;
          border-bottom-left-radius: 4px;
          background-color: #fdfdfd66;
          font-size: $font-small;
          color: $green-color;
          font-weight: 700;
        }

        .overlay {
          position: absolute;
          left: 0;
          top: 80%;
          display: flex;
          flex-direction: column;
          border-radius: 32px;
          padding: 30px 20px 20px;
          height: 100%;
          background: rgba(255, 255, 255, 0.2);
          transition: all 2s ease-in-out;
          backdrop-filter: blur(6px);
          text-align: left;

          &__info {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 38px;
            .overlay__title {
              .overlay__name {
                font-size: $font-medium;
                color: $secondary-color;
                font-weight: 700;
                margin-bottom: 4px;
              }

              .overlay__name-descr {
                font-size: $font-small;
                color: $secondary-color;
                font-weight: 400;
              }
            }
            .overlay__price {
              font-size: $font-price;
              color: $secondary-color;
              font-weight: 700;
              background-color: #ffffff4d;
              border-radius: 4px;
              padding: 8px 16px;
            }
          }

          .overlay__descr {
            font-size: $font-input;
            color: $secondary-color;
            font-weight: 400;
            line-height: 150%;
          }

          .overlay__btn {
            margin-top: auto;
            width: 176px;
            height: 44px;
          }
        }
      }
    }
  }
}
</style>

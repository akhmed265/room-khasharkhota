<template>
  <section class="about">
    <div class="container">
      <div class="about__wrapper">
        <div class="about__media">
          <img src="../assets/image/about.png" alt="" class="about__image" />
          <img
            src="../assets/image/about-video.avif"
            alt=""
            class="about__image about__video"
          />
        </div>

        <div class="about__content">
          <p class="about__subtitle subtitle">о нашем походе</p>
          <h2 class="about__title">
            Исследуйте все горные массивы мира вместе с нами
          </h2>
          <p class="about__text">
            Его корни уходят в один фрагмент классической латыни 45 года н. э.,
            то есть более двух тысячелетий назад. Ричард МакКлинток, профессор
            латыни из колледжа Hampden-Sydney, штат Вирджиния, взял одно из
            самых странных слов в Lorem Ipsum, «consectetur» и занялся его
            поисками в классической латинской литературе.
          </p>

          <Button variant="dark-to-light" type="button">
            Программа тура
          </Button>
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

.about {
  font-family: $font-nunito;

  .container {
    padding: 100px 370px;
  }

  &__wrapper {
    display: flex;
    justify-content: space-between;

    .about__media {
      position: relative;
      width: 480px;
      height: 534px;
      margin-right: 250px;

      .about__image {
        width: 350px;
        height: 400px;
        object-fit: cover;
        border-radius: 24px;
      }

      .about__video {
        position: absolute;
        top: 126px;
        left: 130px;
        object-fit: cover;
      }
    }

    .about__content {
      padding: 64px 0;
      .about__subtitle {
        font-size: $font-medium;
        color: $yellow-color;
        font-weight: 400;
        margin-bottom: 8px;
      }

      .about__title {
        font-size: $font-large;
        color: $text-color;
        font-weight: 800;
        margin-bottom: 40px;
      }

      .about__text {
        font-size: $font-nav;
        color: $text-color;
        font-weight: 400;
        margin-bottom: 40px;
        line-height: 150%;
      }
    }
  }
}
</style>

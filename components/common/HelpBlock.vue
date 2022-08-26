<template>
  <div class="help">
    <div class="container">
      <h2 class="help__title">Нужна помощь с&nbsp;подбором детали?</h2>
      <p class="help__side">
        Оставьте заявку и наш специалист свяжется с Вами
        в ближайшее время. <br><span class="help__free">Это бесплатно!</span></p>
      <div class="help-inputs">
        <BaseInput class="help-inputs__item" placeholder="Ваше имя"/>
        <BaseInput class="help-inputs__item" placeholder="Ваш телефон"/>
        <BaseButton :filled="true" title="Получить консультацию"/>
      </div>
    </div>
  </div>
</template>

<script>
import BaseInput from "~/components/common/BaseInput";
export default {
  name: "HelpBlock",
  components: {BaseInput}
}
</script>

<style lang="scss" scoped>
  .help {
    padding: 54px 0 96px;
    text-align: center;
    position: relative;
    background: linear-gradient(270deg, #9A71FB 0%, #8B5DFA 65.63%);
    &::after {
      content: '';
      left: 0;
      top: 0;
      bottom: 0;
      right: 0;
      background-image: url("@/static/help-block/background.svg");
      position: absolute;
      background-size: cover;
    }
    &__bg {
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
      pointer-events: none;
      z-index: -1;
    }
    &__free {
      font-weight: 600;
      color: #fff;
      font-size: $normal;
    }
    &__title {
      color: #fff;
      font-weight: 600;
      font-size: 22px;
      padding: 0 14px;
      line-height: 130%;
    }
    &__side {
      margin-top: 20px;
      line-height: 140%;
      color: #fff;
      font-size: $normal;
    }
    &-inputs {
      &__item {
        margin-top: 14px;
      }
    }
  }
</style>

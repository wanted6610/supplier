<template>
  <div class="company">
    <div class="container">
      <p class="company__anchor">/ О компании</p>
      <h2 class="company__title">ВашПоставщик — компания, основанная в 2017 году</h2>
      <div class="company-offer">
        <p class="company-offer__item">ВашПоставщик – интренет-магазин с крупнейшим наличием б/у двигателей и коробок передач для легковых автомоблей и коммерческого транспорта.</p>
        <p class="company-offer__item">В своей работе мы охватываем все регионы РФ. Наши представительства уже есть в городах: Нижний Новгород (головной офис), Бор, Чебоксары, Сургут, Санкт-Петербург, Тверь и Симферополь.</p>
      </div>
      <div class="company-list">
        <div class="company-list__item">
          <svg-icon class="company-list__ico" name="ok-icon" width="24" height="24" />
          <p class="company-list__text">Работаем по 45 брендам мировых автопроизводителей</p>
        </div>
        <div class="company-list__item">
          <svg-icon class="company-list__ico" name="ok-icon" width="24" height="24" />
          <p class="company-list__text">Наличие ДВС и КПП всех типов</p>
        </div>
        <div class="company-list__item">
          <svg-icon class="company-list__ico" name="ok-icon" width="24" height="24" />
          <p class="company-list__text">Полный пакет сопроводительных документов, подтверждающий легальность ввоза на территорию РФ и возможность постановки на учёт в ГИБДД</p>
        </div>
      </div>
      <div class="company__image">
        <img class="company__img" src="@/static/company-info/motor.png" />
        <img class="company__bg" src="@/static/company-info/background.svg" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CompanyInfo"
}
</script>

<style lang="scss" scoped>
  .company {
    &__anchor {
      color: $purple;
      font-size: $large;
      font-weight: 600;
    }
    &__title {
      font-weight: 600;
      font-size: $big;
      margin-top: 14px;
      line-height: 130%;
    }
    &-offer {
      margin-top: 22px;
      &__item {
        margin-top: 15px;
        font-size: $normal;
        line-height: 140%;
        &:first-child {
          margin-top: 0;
        }
      }
    }
    &-list {
      margin-top: 38px;
      &__item {
        display: flex;
        margin-top: 20px;
        &:first-child {
          margin-top: 0;
        }
      }
      &__ico {
        min-width: 24px;
        min-height: 24px;
      }
      &__text {
        margin-left: 16px;
        font-size: $normal;
      }
    }
    &__image {
      display: flex;
      margin-top: 92px;
      justify-content: center;
      position: relative;
    }
    &__bg {
      position: absolute;
      z-index: -1;
      left: 50%;
      top: 42%;
      transform: translate(-50%, -50%) rotate(0deg);
    }
  }
</style>

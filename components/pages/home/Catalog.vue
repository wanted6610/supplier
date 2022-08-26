<template>
  <div class="catalog">
    <div class="container">
      <h2 class="catalog__title">Каталог</h2>
      <p class="catalog__side">
        С помощью нашего каталога вы можете самостоятельно найти необходимую
        вам деталь или оставить <span class="catalog__offer">заявку</span>, чтобы уточнить наличие и цену по телефону</p>
      <div class="catalog-categories">
        <div class="catalog-categories__item catalog-categories__item_motor">
          <div class="catalog-categories__offer">
            <p class="catalog-categories__text">Выбрать двигатель</p>
            <svg-icon name="arrow-icon" width="24" height="15" />
          </div>
        </div>
        <div class="catalog-categories__item catalog-categories__item_kpp">
          <div class="catalog-categories__offer">
            <p class="catalog-categories__text">Выбрать КПП</p>
            <svg-icon name="arrow-icon" width="24" height="15" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Catalog"
}
</script>

<style lang="scss" scoped>
  .catalog {
    &__title {
      font-size: $big;
      font-weight: 600;
      text-align: center;
    }
    &__side {
      margin-top: 18px;
      line-height: 140%;
      text-align: center;
    }
    &__offer {
      color: $purple;
      text-decoration: underline;
      cursor: pointer;
      font-weight: 600;
    }
    &-categories {
      margin-top: 52px;
      &__item {
        min-height: 231px;
        background-size: cover;
        border-radius: 16px;
        display: flex;
        align-items: flex-end;
        margin-top: 16px;
        &:first-child {
          margin-top: 0;
        }
        &_motor {
          background-image: url("@/static/catalog/change-motor.png");
        }
        &_kpp {
          background-image: url("@/static/catalog/change-kpp.png");
        }
      }
      &__text {
        color: #fff;
        font-weight: 600;
        font-size: 20px;
        margin-right: 14px;
      }
      &__offer {
        display: flex;
        align-items: center;
        padding: 20px 30px;
      }
    }
  }
</style>

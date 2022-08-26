<template>
  <div class="slider">
    <div class="slider-content">
      <div class="slide">
        <div class="slide__text">
          <h3 class="slide__title">>30 000 <br>позиций</h3>
          <p class="slide__desc">Самая большая база<br> контрактных<br> ДВС и КПП в наличии</p>
        </div>
        <span class="slide__number slide__number_one">1</span>
      </div>
      <div class="slide">
        <div class="slide__text">
          <h3 class="slide__title">Гарантия<br> качества</h3>
          <p class="slide__desc">Документальное<br> подтверждение технической<br> исправности товара</p>
        </div>
        <span class="slide__number slide__number_two">2</span>
      </div>
      <div class="slide">
        <div class="slide__text">
          <h3 class="slide__title">Доставка<br> в любой регион РФ</h3>
          <p class="slide__desc">От 2 до 20 дней<br> с возможностью<br> отслеживания товара</p>
        </div>
        <span class="slide__number slide__number_three">3</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BaseSwiper",
}
</script>

<style lang="scss" scoped>
  .slider {
    margin-top: 76px;
    overflow: hidden;
    &-content {
      display: flex;
      padding: 0 16px;
      overflow-x: scroll;
      -ms-overflow-style: none;
      scrollbar-width: none;
      &::-webkit-scrollbar {width: 0 !important;}
    }
  }
  .slide {
    min-width: 202px;
    min-height: 100px;
    padding: 15px 20px;
    background: rgba(125, 125, 125, 0.3);
    margin-right: 16px;
    border-radius: 22px;
    position: relative;
    overflow: hidden;
    z-index: 1;
    flex: 1;
    &:last-child {
      margin-right: 0;
    }
    &__title {
      color: $purple;
      font-size: $normal;
      font-weight: 700;
    }
    &__text {
      text-align: left;
    }
    &__desc {
      color: #fff;
      font-size: $regular;
    }
    &__number {
      position: absolute;
      font-size: 206px;
      font-family: 'Lilita One', cursive;
      z-index: -1;
      color: transparent;
      -webkit-text-stroke-width: 1px;
      -webkit-text-stroke-color: #8D8D8E;
      &_one {
        right: 2px;
        top: 90px;
        transform: rotate(16deg);
      }
      &_two {
        top: 30px;
        right: -15px;
        transform: rotate(344deg);
      }
      &_three {
        transform: rotate(32deg);
        bottom: 0;
      }
    }
  }
</style>

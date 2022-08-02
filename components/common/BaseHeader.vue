<template>
  <header class="header">
    <div class="container">
      <div class="header-main">
        <nuxt-link to="/" exact class="header-main__link">
          <img src="@/static/main-logo.png" alt="Ваш поставщик" class="header__logo">
        </nuxt-link>
        <div class="header-buttons">
          <nuxt-link to="/cart" class="header-buttons__cart">
            <svg-icon width="27" height="26" name="cart-icon" />
            <span class="header-buttons__count">99</span>
          </nuxt-link>
          <svg-icon width="34" height="20" name="burger-icon" class="header-buttons__burger" />
        </div>
      </div>
    </div>
    <hr class="header__separator" />
    <BaseHeaderSearch v-if="$route.path === '/'" />
  </header>
</template>

<script>
import mainMenu from "~/mixins/mainMenu";
import BaseHeaderSearch from "~/components/common/BaseHeaderSearch";

export default {
  name: "BaseHeader",
  components: {
    BaseHeaderSearch,
  },

  mixins: [mainMenu],
}
</script>

<style lang="scss" scoped>
  .header {
    margin-bottom: 38px;
    &__logo {
      width: 129px;
      height: 27px;
    }
    &__separator {
      height: 1px;
      background: $gray;
      margin: 0;
      border: none;
    }
    &-main {
      padding: 15px 0 18px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      &__link {
        &::after {display: none}
      }
    }
    &-buttons {
      display: flex;
      align-items: center;
      &__burger {
        margin-left: 32px;
      }
      &__cart {
        position: relative;
        &::after {display: none}
      }
      &__count {
        position: absolute;
        padding: 3px 3px;
        background: $purple;
        color: #fff;
        border-radius: 50%;
        min-height: 19px;
        min-width: 19px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: $small;
        bottom: -8px;
        right: -19px;
      }
    }
  }
</style>

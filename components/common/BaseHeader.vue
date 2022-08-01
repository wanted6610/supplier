<template>
  <header class="header">

    <!--top header-->
    <div class="container">
      <nav class="menu">
        <ul class="menu-list">
          <li class="menu-list__item" v-for="link in menu">
            <nuxt-link :to="link.link">{{ link.label }}</nuxt-link>
          </li>
        </ul>
      </nav>
    </div>
    <!--top header end-->

    <hr class="header__separator" />

    <!--side header-->
    <div class="container">
      <div class="info">
        <svg-icon fill="red" name="main-logo" width="290" height="61" />
      </div>
    </div>
    <!--side header end-->

  </header>
</template>

<script>
import mainMenu from "~/mixins/mainMenu";

export default {
  name: "BaseHeader",
  mixins: [mainMenu],
}
</script>

<style lang="scss" scoped>
  .menu {
    padding: 60px 0 40px;
    &-list {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
  }
  .header {
    &__separator {
      height: 2px;
      color: red;
      background-color: $gray;
      border: none;
    }
  }
  .info {
    margin-top: 44px;
  }
</style>

<template>
  <footer class="footer">
    <div class="container">
      <svg-icon name="main-logo" class="footer__logo" />
      <div class="footer-links">
        <div class="footer-links__column">
          <nuxt-link to="/" class="footer-links__link">Главная</nuxt-link>
          <nuxt-link to="/" class="footer-links__link">О компании</nuxt-link>
          <nuxt-link to="/" class="footer-links__link">Каталог ДВС</nuxt-link>
          <nuxt-link to="/" class="footer-links__link">Каталог КПП</nuxt-link>
        </div>
        <div class="footer-links__column">
          <nuxt-link to="/" class="footer-links__link">Этапы работы</nuxt-link>
          <nuxt-link to="/" class="footer-links__link">Оплата заказа</nuxt-link>
          <nuxt-link to="/" class="footer-links__link">Отзывы</nuxt-link>
          <nuxt-link to="/" class="footer-links__link">Контакты</nuxt-link>
        </div>
      </div>
      <base-button
        class="footer__btn"
        title="Задать вопрос"
      />
      <div class="footer-contacts">
        <a href="tel:89047853359" class="footer-contacts__phone">+7 (904) 785-33-59</a>
        <div class="footer-contacts__links">
          <a href="" class="footer-contacts__link">Viber</a>
          <a href="" class="footer-contacts__link separator">WhatsApp</a>
          <a href="" class="footer-contacts__link">Telegram</a>
        </div>
      </div>
      <hr class="footer__separator" />
      <div class="footer-documents">
        <a href="#" class="footer-documents__document">Политика конфидециальности</a>
        <a href="#" class="footer-documents__document">Соглашение на обработку<br> персональных данных</a>
        <a href="#" class="footer-documents__document">Договор оферты</a>
      </div>
    </div>
  </footer>
</template>

<script>
import mainMenu from "~/mixins/mainMenu";

export default {
  mixins: [mainMenu],
  name: "BaseFooter"
}
</script>

<style lang="scss" scoped>
  .footer {
    padding: 54px 0 46px;
    &__logo {
      width: 172px;
      height: 38px;
    }
    &__separator {
      border: none;
      height: 1px;
      background: $secondary-gray;
      margin: 36px 0;
    }
    &__btn {
      margin-top: 66px;
    }
    &-documents {
      &__document {
        margin-top: 22px;
        display: block;
        color: $secondary-gray;
        font-size: $regular;
        &:first-child {
          margin-top: 0;
        }
      }
    }
    &-contacts {
      margin-top: 22px;
      &__phone {
        font-size: $normal;
        font-weight: 600;
      }
      &__links {
        margin-top: 8px;
        display: flex;
      }
      &__link {
        color: $secondary-gray;
        font-size: $regular;
        font-weight: 400;
        margin-left: 12px;
        position: relative;
        &::before {
          content: '';
          position: absolute;
          height: 100%;
          width: 1px;
          background: $secondary-gray;
          left: -5px;
        }
        &:first-child {
          margin-left: 0;
          &::before {
            display: none;
          }
        }
      }
    }
    &-links {
      display: flex;
      align-items: center;
      gap: 70px;
      margin-top: 46px;
      &__link {
        font-size: $normal;
        font-weight: 400;
        margin-top: 22px;
        &:first-child{margin-top: 0;}
        &::after {display: none}
      }
      &__column {
        display: flex;
        flex-direction: column;
      }
    }
  }
</style>

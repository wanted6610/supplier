<template>
  <div class="contacts">
    <div class="container">
      <img src="@/static/contacts-block/wave.png" alt="wave" class="contacts__wave">
      <h3 class="contacts__title">Контакты</h3>
      <div class="contacts-address contacts-text">
        <p class="contacts-address__title contacts-text__title">Адрес</p>
        <p class="contacts-address__value contacts-text__value">Нижегородская область,<br> г. Дзержинск, Гастелло 6А</p>
      </div>
      <div class="contacts-phone contacts-text">
        <p class="contacts-phone__title contacts-text__title">Телефон</p>
        <p class="contacts-phone__value contacts-text__value">+7 (831) 219-96-19</p>
      </div>
      <div class="contacts-mail contacts-text">
        <p class="contacts-mail__title contacts-text__title">Email:</p>
        <p class="contacts-mail__value contacts-text__value">yoursupplier-avto@yandex.ru</p>
      </div>
      <div class="contacts-write contacts-text">
        <p class="contacts-write__title contacts-text__title">Напишите нам:</p>
        <div class="contacts-write__icons">
          <svg-icon name="social/viber-icon" width="30" height="30" />
          <svg-icon name="social/whatsup-icon" width="30" height="30" />
          <svg-icon name="social/telegram-icon" width="30" height="30" />
          <svg-icon name="social/vk-icon" width="30" height="30" />
        </div>
        <div class="contacts-map" v-if="mapLoaded">
          <yandex-map
            class="contacts-map__ymap"
            :settings="mapSettings"
            :zoom="15"
            :coords="[56.244410, 43.468246]"
          >
            <ymap-marker
              :coords="[56.244410, 43.468246]"
              :marker-id="0"
              hint-content="some"
              :icon="{color: 'red'}"
              @click="openCompanyInfo"
            />
          </yandex-map>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { yandexMap, ymapMarker } from 'vue-yandex-maps'

export default {
  name: "ContactsBlock",
  data() {
    return {
      mapSettings: {
        apiKey: '024d4226-b055-43bf-b765-9bf8b86a0410',
        lang: 'ru_RU',
        coordorder: 'latlong',
        enterprise: false,
        version: '2.1',
      },
      mapLoaded: false,
    }
  },
  components: {
    yandexMap,
    ymapMarker,
  },
  mounted() {
    this.mapLoaded = true;
  },
  methods: {
    openCompanyInfo() {
      window.open('https://yandex.ru/maps/-/CCURm6QeKD', '_blank');
    }
  }
}
</script>

<style lang="scss" >

  .contacts-map__ymap div * ymaps {
    border-radius: 28px;
  }

  .contacts {
    background: #2E2B37;
    padding: 42px 0 16px;
    position: relative;
    &-map {
      height: 320px;
      width: 100%;
      margin-top: 32px;
      border-radius: 28px;
      &__ymap {
        height: 100%;
        border-radius: 28px;
      }
    }
    &__wave {
      position: absolute;
      right: 0;
      top: 0;
      pointer-events: none;
    }
    & p {
      color: #fff;
      font-size: $normal;
    }
    & h3 {
      color: $purple;
      font-size: $big;
      font-weight: 600;
    }
    &-text {
      margin-top: 26px;
      &__title {
        font-weight: 600;
      }
      &__value {
        font-weight: 400;
        margin-top: 10px;
      }
    }
    &-write {
      &__icons {
        margin-top: 10px;
        display: flex;
        align-items: center;
        gap: 11px;
      }
    }
  }
</style>

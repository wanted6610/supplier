<template>
  <div class="main">
    <section class="offer">
      <h1 class="offer__title">Продажа оригинальных контрактных ДВС и КПП</h1>
      <p class="offer__side">Профильный магазин контрактных двигателей и КПП с разборов Японии, Кореи, США и стран Европы</p>
      <BaseButton
        class="offer__btn"
        title="Оставить заявку"
        :filled="true"
      />
      <OfferSwiper />
    </section>
    <section class="company-section">
      <CompanyInfo />
    </section>
    <section class="catalog-section">
      <Catalog />
    </section>
    <div class="need-help">
      <HelpBlock />
    </div>
    <section class="work">

    </section>
    <section class="pay">

    </section>
    <section class="questions">

    </section>
    <section class="about">

    </section>
    <contacts-block />
  </div>
</template>

<script>
import ContactsBlock from "~/components/pages/home/ContactsBlock";
import BaseButton from "~/components/common/BaseButton";
import OfferSwiper from "~/components/pages/home/OfferSwiper";
import CompanyInfo from "~/components/pages/home/CompanyInfo";
import Catalog from "~/components/pages/home/Catalog";
import HelpBlock from "~/components/common/HelpBlock";
export default {
  name: 'IndexPage',
  components: {HelpBlock, Catalog, CompanyInfo, OfferSwiper, ContactsBlock, BaseButton},
  data() {
    return {
    }
  }
}
</script>

<style lang="scss" scoped>
.offer {
  text-align: center;
  padding: 52px 0 33px;
  background:linear-gradient(rgba(0, 0, 0, 0.58), rgba(0, 0, 0, 0.58)), url("@/static/main-page/offer-bg.png");
  background-size: cover;
  &__title {
    color: #fff;
    font-size: $biggest;
    font-weight: 600;
    line-height: 120%;
    padding: 0 50px;
  }
  &__side {
    margin-top: 24px;
    color: #fff;
    padding: 0 34px;
  }
  &__btn {
    margin-top: 34px;
    display: flex;
    justify-content: center;
  }
}
.company-section {
  margin-top: 56px;
}

.catalog-section {
  margin-top: 110px;
}

.need-help {
  margin-top: 72px;
}
</style>

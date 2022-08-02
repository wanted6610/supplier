<template>
  <div class="search">
    <div class="container">
      <BaseInput
        class="search__input"
        :with-icon="true"
        icon-name="search-icon"
        placeholder="Поиск по каталогу"
      />
    </div>
  </div>
</template>

<script>
import BaseInput from "~/components/common/BaseInput";
export default {
  name: "BaseHeaderSearch",
  components: {BaseInput}
}
</script>

<style lang="scss" scoped>
  .search {
    &__input {
      margin-top: 14px;
    }
  }
</style>

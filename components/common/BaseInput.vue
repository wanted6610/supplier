<template>
  <div class="input">
    <input type="text" :placeholder="placeholder" class="input__main" :class="{'with-icon': withIcon}">
    <div v-if="withIcon" class="input-icon">
      <svg-icon :name="iconName" width="18" height="18" />
    </div>
  </div>
</template>

<script>
export default {
  name: "BaseInput",
  props: {
    withIcon: {
      type: Boolean,
      default: false,
    },
    iconName: {
      type: String,
      default: 'search-icon'
    },
    placeholder: {
      type: String,
      default: 'Поиск'
    }
  }
}
</script>

<style lang="scss" scoped>
  .input {
    display: flex;
    flex: 1;
    position: relative;
    &__main {
      min-height: 44px;
      border: 1px solid $gray;
      flex: 1;
      padding: 0 20px;
      border-radius: 52px;
      font-size: $regular;
      &.with-icon {padding-right: 56px;}
      &::placeholder {
        color: $light-gray;
      }
    }
    &-icon {
      background: $purple;
      border-radius: 50%;
      width: 44px;
      height: 44px;
      position: absolute;
      display: flex;
      justify-content: center;
      align-items: center;
      right: 0;
      top: 50%;
      transform: translateY(-50%);
    }
  }
</style>

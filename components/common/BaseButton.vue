<template>
  <div class="button">
    <button
      class="btn"
      type="button"
      :class="[{'outline': outline}]"
      >{{title}}
    </button>
  </div>
</template>

<script>
export default {
  name: "BaseButton",
  props: {
    title: {
      type: String,
      default: 'Кнопка'
    },
    outline: {
      type: Boolean,
      default: true,
    }
  }
}
</script>

<style lang="scss" scoped>
.btn {
  &.outline {
    border: 2px solid $purple;
    border-radius: 40px;
    padding: 19px 43px;
    color: $purple;
    font-size: $normal;
    font-weight: 600;
  }
}
</style>

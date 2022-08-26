<template>
  <div class="button">
    <button
      class="btn"
      @click="btnClick"
      type="button"
      :class="[{'outline': outline, 'filled': filled}]"
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
    },
    filled: {
      type: Boolean,
      default: false,
    }
  },
  methods: {
    btnClick() {
      console.log('btn clicked!')
    }
  }
}
</script>

<style lang="scss" scoped>
.button {width: 100%}
.btn {
  padding: 19px 43px;
  border-radius: 40px;
  font-size: $normal;
  font-weight: 600;
  &.outline {
    border: 2px solid $purple;
    color: $purple;
    background: inherit;
  }
  &.filled {
    background: $purple;
    color: #fff;
    border: none;
  }
}
</style>

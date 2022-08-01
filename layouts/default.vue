<template>
  <div class="main">
    <base-header />
    <nuxt />
  </div>
</template>

<script>
import BaseHeader from "~/components/common/BaseHeader";

export default {
  name: "default",
  components: {
    BaseHeader,
  }
}
</script>

<style lang="scss">

a.nuxt-link-active {
  font-weight: 600;
  position: relative;
  &:after {
    content: '';
    position: absolute;
    left: 0;
    right: 0;
    height: 3px;
    background: $purple;
    bottom: -12px;
    border-radius: 30px;
  }
}

</style>

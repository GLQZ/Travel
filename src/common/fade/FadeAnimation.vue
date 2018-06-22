<template>
  <transition>
    <slot></slot>
  </transition>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'FadeAnimation'
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  .v-enter, .v-leave-to
    opacity 0
  .v-enter-active, .v-leave-active
    transition opacity 1s
</style>

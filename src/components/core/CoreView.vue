<template>
  <transition name="component-fade" mode="out-in">
    <router-view></router-view>
  </transition>
</template>

<script>
  export default {};
</script>

<style lang="scss" scoped>
  .component-fade-enter-active,
  .component-fade-leave-active {
    transition: opacity 0.3s ease;
  }
  .component-fade-enter, .component-fade-leave-to
/* .component-fade-leave-active below version 2.1.8 */ {
    opacity: 0;
  }
</style>

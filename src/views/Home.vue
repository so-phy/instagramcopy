<template>
  <div class="home">
    <div class="home-content">
      <core-app-bar></core-app-bar>
      <core-view></core-view>
    </div>
  </div>
</template>

<script>
  // @ is an alias to /src

  export default {
    name: 'Home',
    components: {
      CoreAppBar: () => import('@/components/core/AppBar.vue'),
      CoreView: () => import('@/components/core/CoreView.vue'),
    },
  };
</script>
<style lang="scss" scoped>
  .home {
    background-color: #e7e7e7;
    display: flex;
    flex-flow: row;
    justify-content: center;
  }
  .home-content {
    background-color: white;
    min-width: 560px;
    min-height: 100vh;
  }
</style>

<template>
  <div>
    <story-slider></story-slider>
  </div>
</template>

<script>
  export default {
    name: 'Main',
    components: {
      StorySlider: () => import('@/components/main/StorySlider.vue'),
    },
  };
</script>

<style lang="scss" scoped></style>

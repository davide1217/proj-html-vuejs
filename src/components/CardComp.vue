<template>
  <div class="_col col-6 col-lg-3">
    <img :src="`${require('@/assets/images/' + image + '.jpg')}`" alt="">
    <div>
      <span>{{title}}</span>
    </div>
  </div>
</template>

<script>
export default {
name: 'CardComp',

  props: {
    image: String,
    title: String,
  },
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/_vars';
@import '@/assets/styles/_mixins';
  ._col {
  position: relative;
  display: flex;
  justify-content: center;

    & img {
      width: 100%;
    }

    & > div {
      @include flex;
      opacity: 0;
      width: 0;
      height: 100%;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      transition: all 1s;
    }

    &:hover > div {
      opacity: 1;
      width: 100%;
      background-color: rgba($color: $yellow, $alpha: .5);
    }

    & span {
      text-transform: uppercase;
      font-size: 1.5rem;
    }
  }
</style>
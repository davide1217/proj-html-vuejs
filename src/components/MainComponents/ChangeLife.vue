<template>
  <section>
    <div class="container60">
      <h3>change a life today</h3>
      <div class="line"></div>
      <span>As long as poverty, injustice and inequality persist, none of us can truly rest. It doesn't take much to change a life. Get in touch today and start making the difference.</span>
      <div class="bottons mt-5">
        <a class="_btn white mx-4 my-2">volunteer</a>
        <a class="_btn white mx-4 my-2">donate now</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ChangeLife'
}
</script>

<style lang="scss" scoped>
@import '../../assets/styles/_mixins';

  section {
    height: 70vh;
    background-image: url(../../assets/images/home-footer.jpg);
    background-position: center;

    & > div {
      @include flex-column;
      text-align: center;
    }
  }

  h3 {
    color: white;
  }
</style>
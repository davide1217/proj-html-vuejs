<template>
  <div id="jumbotron">
    <section class="container50">
      <h1 class="text-uppercase mb-2">make a difference</h1>
      <p>As long as poverty, injustice and inequality persist, none of us can trult rest</p>
      <a class="_btn white mx-2" href="#2">our mission</a>
      <a class="_btn yellow mx-2" href="#">donate now</a>
    </section>
  </div>
</template>

<script>
export default {
  name: 'JumboTron',
}
</script>

<style lang="scss" scoped>

  #jumbotron {
    height: 100vh;
    background-image: url(../assets/images/home-page-slider.jpg);
    background-size: cover;
    background-position: center;
    display: flex;
    justify-content: center;
    align-items: center;
    
    section {
      text-align: center;

      & p {
        margin-bottom: 30px;
      }
    }
  }
</style>
<template>
  <section id="2">
    <div class="container90">
      <h3>recent causes</h3>
      <div class="line"></div>
      <span>We run projects in over 30 countries in 5 continents</span>
      <div id="images">
        <img src="../../assets/images/avada-charity-fair-trade-featured-400x300.jpg" alt="">
        <img src="../../assets/images/avada-charity-shelter-featured-400x300.jpg" alt="">
        <img src="../../assets/images/avada-charity-farming-featured-400x300.jpg" alt="">
        <img src="../../assets/images/avada-charity-vaccines-featured-400x300.jpg" alt="">
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'RecentCauses',
}
</script>

<style lang="scss" scoped>
@import '../../assets/styles/_vars';

  section {
    padding: 70px 0;
  }

  span {
    color: $grey;
  }

  #images {
    display: flex;
    justify-content: center;
    width: 90%;
    margin-top: 70px;

    & img {
      width: 25%;
      padding: 0 10px;
    }
  }
</style>
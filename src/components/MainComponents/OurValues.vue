<template>
  <section>
    <div class="container90">
      <h3 class="white">our values</h3>
      <div class="line"></div>
      <span>Think Big. Act Bigger.</span>

      <div class="container-fluid">
        <div class="row flex-wrap values">
          <div class="col-6 col-lg-3">
            <i class="fa-solid fa-droplet"></i>
            <h6>Clean Water</h6>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi aut architecto quaerat accusantium rem.</p>
            <a href="#" class="_btn full">learn more</a>
          </div>

          <div class="col-6 col-lg-3">
            <i class="fa-solid fa-stethoscope"></i>
            <h6>Vaccinations</h6>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi aut architecto quaerat accusantium rem.</p>
            <a href="#" class="_btn full">learn more</a>
          </div>

          <div class="col-6 col-lg-3">
            <i class="fa-solid fa-graduation-cap"></i>
            <h6>Education</h6>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi aut architecto quaerat accusantium rem.</p>
            <a href="#" class="_btn full">learn more</a>
          </div>

          <div class="col-6 col-lg-3">
            <i class="fa-brands fa-pagelines"></i>
            <h6>Farming</h6>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi aut architecto quaerat accusantium rem.</p>
            <a href="#" class="_btn full">learn more</a>
          </div>
          
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'OurValues'
}
</script>

<style lang="scss" scoped>
@import '../../assets/styles/_vars';
@import '../../assets/styles/_mixins';

  section {
    padding: 50px 0;
    background-image: url(../../assets/images/home-content-bg-2.jpg);
    background-size: cover;
    background-position: center;

    & .values {
      margin-top: 5.5rem;
    }
  }

  .values > div {
    @include flex-column;
    padding: 20px 10px;

    & i {
      font-size: 2.3rem;
      color: $yellow;
      margin-bottom: 5px;
    }
     
    & p {
      margin: 13px 0 22px;
      text-align: center;
    }
  }
</style>
<template>
  <section class="d-flex align-items-center">
    <div class="h-75 container90 d-flex flex-column align-items-center">
      <h3 class="white">our values</h3>
      <div class="line"></div>
      <span>Think Big. Act Bigger.</span>

      <div class="w-100 values d-flex">
        <div>
          <i class="fa-solid fa-droplet"></i>
          <h6>Clean Water</h6>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi aut architecto quaerat accusantium rem.</p>
          <a href="#" class="_btn full">learn more</a>
        </div>

        <div>
          <i class="fa-solid fa-stethoscope"></i>
          <h6>Vaccinations</h6>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi aut architecto quaerat accusantium rem.</p>
          <a href="#" class="_btn full">learn more</a>
        </div>

        <div>
          <i class="fa-solid fa-graduation-cap"></i>
          <h6>Education</h6>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi aut architecto quaerat accusantium rem.</p>
          <a href="#" class="_btn full">learn more</a>
        </div>

        <div>
          <i class="fa-brands fa-pagelines"></i>
          <h6>Farming</h6>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi aut architecto quaerat accusantium rem.</p>
          <a href="#" class="_btn full">learn more</a>
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

  section {
    height: 70vh;
    background-image: url(../../assets/images/home-content-bg-2.jpg);
    background-size: cover;
    background-position: center;

    & .values {
      margin-top: 5.5rem;
    }
  }

  .values > div {
    display: flex;
    flex-direction: column;
    align-items: center;
    flex-basis: 25%;
    padding: 0 7px;

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
<template>
  <header>
    <div class="container90">
      <div class="container-fluid h-100">
        <div class="row h-100 align-items-center">
          
          <div class="col-8 col-sm-6 col-md-4 col-lg-3">
            <img class="w-100" src="../assets/images/avada-charity-logo.png" alt="">
          </div>

          <div class="d-none d-md-inline-block col-md-8 col-lg-9 text-end">
            <ul>
              <HeaderMenu v-for="(item, index) in menu" :key="`m-${index}`"
               :text="item" :index="index" :menu="menu"/>
            </ul>
          </div>

        </div>
      </div>
    </div>

    <div class="text-center">
      <h1 class="text-uppercase mb-2">make a difference</h1>
      <p>As long as poverty, injustice and inequality persist, none of us can trult rest</p>
      <div class="bottons">
        <a class="_btn white m-2" href="#2">our mission</a>
        <a class="_btn yellow m-2" href="#">donate now</a>
      </div>
    </div>

    <a href="#" id="get-back">
      <i class="fa-solid fa-chevron-up"></i>
    </a>
  </header>
</template>

<script>
import HeaderMenu from './HeaderMenu'


export default {
  components: { HeaderMenu },
  name: 'HeaderComp',
  data() {
    return {
      menu: [ 'home', 'mission', 'causes', 'journal', 'donate']
    }
  },
}
</script>

<style lang="scss" scoped>
@import '../assets/styles/_mixins';
@import '../assets/styles/_vars';

  header {
    position: relative;
    height: 100vh;
    background-image: url(../assets/images/home-page-slider.jpg);
    background-size: cover;
    background-position: center;
    
    & > div:first-child {
      height: 15vh;
    }

    & > div:last-of-type {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);

      & p {
        margin-bottom: 30px;
      }
    }

  }

  #get-back {
    position: fixed;
    bottom: 0;
    right: 40px;
    padding: 10px 20px;
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
    background-color: $black;
    color: white;
  }
</style>
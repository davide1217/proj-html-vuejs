<template>
  <div id="jumbotron">
    <header>
      <img src="../assets/images/avada-charity-logo.png" alt="">

      <div>
        <ul>
          <li v-for="(item, index) in menu" :key="`m-${index}}`"><a class="text-uppercase" :class="{'_btn full' : index == menu.length - 1}" :href="`#${index}}`">{{item.text}}</a></li>
        </ul>
      </div>
    </header>

    <section>
      <h1 class="text-uppercase mb-2">make a decision</h1>
      <p>As long as poverty, injustice and inequality persist, none of us can trult rest</p>
      <a class="_btn white mx-2" href="#2">our mission</a>
      <a class="_btn yellow mx-2" href="#">donate now</a>
    </section>
  </div>
</template>

<script>
export default {
  name: 'HeaderComp',
  props: {
    menu: Array,
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/styles/_vars';
  #jumbotron {
    height: 100vh;
    background-image: url(../assets/images/home-page-slider.jpg);
    background-size: cover;
    background-position: center;

    header {
      width: 90%;
      height: 15%;
      margin: auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    & img {
      width: 20%;
    }

    & ul {
      list-style: none;

      & li {
        display: inline-block;
        margin: 10px;
        & a {
          font-size: .7rem;
          color: white;
        }

        & a:not(li:last-of-type a):focus {
          color: $yellow;
        }
      }
    }

    section {
      width: 50%;
      margin: 17% auto 0;
      text-align: center;

      & p {
        margin-bottom: 30px;
      }
    }
  }
</style>
<template>
  <div>
    <HeaderComp :menu="menu" />
    <MainComp />
    <FooterComp />
  </div>
</template>

<script>
import FooterComp from './components/FooterComp.vue'
import HeaderComp from './components/HeaderComp.vue'
import MainComp from './components/MainComp.vue'


export default {
  name: 'App',
  components: {
    HeaderComp,
    MainComp,
    FooterComp,
  },
  data() {
    return {
      menu: [
        {
          text: 'home',
        },
        {
          text: 'mission',
        },
        {
          text: 'causes',
        },
        {
          text: 'journal',
        },
        {
          text: 'donate',
        },
      ]
    }
  }
}
</script>
    

<style lang="scss">
@import './assets/styles/_global';

</style>

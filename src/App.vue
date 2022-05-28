<template>
  <div>
    <HeaderComp />
    <JumboTron />
    <MainComp />
    <FooterComp />
  </div>
</template>

<script>
import FooterComp from './components/FooterComp.vue'
import HeaderComp from './components/HeaderComp.vue'
import JumboTron from './components/JumboTron.vue'
import MainComp from './components/MainComp.vue'


export default {
  name: 'App',
  components: {
    HeaderComp,
    MainComp,
    FooterComp,
    JumboTron,
  },
  data() {
    return {
      
    }
  }
}
</script>
    

<style lang="scss">
@import './assets/styles/_global';

</style>

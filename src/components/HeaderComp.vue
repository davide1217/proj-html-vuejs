<template>
  <header class="container90">
    <img src="../assets/images/avada-charity-logo.png" alt="">

    <div>
      <ul>
        <MenuComp v-for="(item, index) in menu" :key="`m-${index}`"
         :text="item" :index="index" :menu="menu"/>
      </ul>
    </div>
  </header>
</template>

<script>
import MenuComp from './MenuComp.vue'


export default {
  components: { MenuComp },
  name: 'HeaderComp',
  data() {
    return {
      menu: [ 'home', 'mission', 'causes', 'journal', 'donate']
    }
  },
}
</script>

<style lang="scss" scoped>

  header {
    position: fixed;
    left: 5%;
    height: 15%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  img {
    width: 20%;
  }

</style>
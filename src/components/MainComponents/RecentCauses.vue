<template>
  <section id="2">
    <div class="container90">
      <h3>recent causes</h3>
      <div class="line"></div>
      <span class="text-center">We run projects in over 30 countries in 5 continents</span>

      <div class="container-fluid _container">
        <div id="images" class="row flex-wrap">
          <CardComp v-for="(image, index) in images" :key="`card-${index}`"
          :image="image.path" :title="image.title" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import CardComp from '../ExtraComp/CardComp.vue'

export default {

  components: { CardComp },

  name: 'RecentCauses',

  data() {
    return {
      images: [
        {
          path: 'avada-charity-fair-trade-featured-400x300',
          title: 'fair trade'
        },
        {
          path: 'avada-charity-shelter-featured-400x300',
          title: 'shelter'
        },
        {
          path: 'avada-charity-farming-featured-400x300',
          title: 'farming'
        },
        {
          path: 'avada-charity-vaccines-featured-400x300',
          title: 'vaccines'
        },
      ]
    }
  }
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
    justify-content: center;
    height: 100%;
    --bs-gutter-x: 0;

    & > ._col {
      transform: scale(.9);
    }
  }

  ._container {
    margin-top: 70px;
  }
</style>
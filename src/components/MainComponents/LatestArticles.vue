<template>
  <section id="3">
    <div class="container60">

        <div class="col-12 d-flex flex-column align-items-center">
          <h3>latest articles</h3>
          <div class="line"></div>
          <span>Together we make all the difference</span>
        </div>

        <div id="articles" class="container-fluid">
          <div class="row h-100">

            <div id="left" class="col-6 col-md-8 col-lg-6">

              <div id="imgBig" class="row w-100">
                <CardComp :image="articles[activeArticleIndex].imageBig"
                :title="articles[activeArticleIndex].title" />
              </div>

              <div class="p-3">
                <h6>{{articles[activeArticleIndex].title}}</h6>
                <p>{{articles[activeArticleIndex].description}}</p>
              </div>
            </div>

            <div id="right" class="col-6 d-flex flex-column align-items-center d-lg-inline-block col-md-4 col-lg-6">

              <div v-for="(article, index) in articles" 
              :key="index"
              @click="activeArticle(index)">

                <img :src="`${require('../../assets/images/' + article.imageLittle + '.jpg')}`" :alt="article.title">

                <div class="ps-3 d-none d-lg-inline-block">
                  <h6>{{article.title}}</h6>
                  <p>{{article.description}}</p>
                </div>

              </div>
            </div>
          </div>
        </div>

      <div class="_btn red">view all our articles</div>

    </div>
  </section>
</template>

<script>
import CardComp from '../ExtraComp/CardComp.vue';


export default {
  components: { CardComp },

  name: 'LatestArticles',

  data() {
    return {
      activeArticleIndex: 0,

      articles: [
        {
          title: 'Understanding community  complexities',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat quidem magni iure quos a. Eius.',
          imageBig: 'photo-1444213007800-cff19e1677ac-600x450',
          imageLittle: 'photo-1444213007800-cff19e1677ac-200x150',
        },
        {
          title: 'The uman story of uniqueness',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat quidem magni iure quos a. Eius.',
          imageBig: 'photo-1444664597500-035db93e2323-177x142',
          imageLittle: 'photo-1444664597500-035db93e2323-177x142',
        },
        {
          title: 'Sustainable trade tactics',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat quidem magni iure quos a. Eius.',
          imageBig: 'photo-1447430617419-95715602278e-177x142',
          imageLittle: 'photo-1447430617419-95715602278e-177x142',
        },
        {
          title: 'Farmers making a difference',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat quidem magni iure quos a. Eius.',
          imageBig: 'photo-1460230525622-630fe3294cd7-177x142',
          imageLittle: 'photo-1460230525622-630fe3294cd7-177x142',
        },
        {
          title: 'Meeting remote tribes in Peru',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat quidem magni iure quos a. Eius.',
          imageBig: 'photo-1460600421604-5e138c208b9c-177x142',
          imageLittle: 'photo-1460600421604-5e138c208b9c-177x142',
        },
      ]
    }
  },

  methods: {
    activeArticle(index) {
      this.activeArticleIndex = index;
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/styles/_vars';

  section {
    padding: 70px 0;
    background-color: #F5F5F5;
  }

  span {
    color: $grey;
  }

  #articles {
    height: 55vh;
    margin-top: 50px;
  }

  #left {
      height: 100%;
      overflow-y: auto;
      padding: 0;

      & > div:last-of-type {
        border: 1px solid lighten($light-grey, 25%);
        border-bottom: 3px solid lighten($light-grey, 25%);
      }

      & img {
        width: 100%;
      }

      & p {
        height: 20%;
        margin-bottom: 0;
        overflow-y: auto;
      }
    }

    #right {
      height: 100%;
      overflow-y: auto;
      padding: 0 0 0 30px;

      & > div {
        height: 25%;
        cursor: pointer;
        
        padding-bottom: 20px;
        display: flex;

        & > div {
          height: 100%;
          overflow-y: auto;
        }

        & img {
          max-width: 110px;
          height: 90px;
          transition: all .5s;
        }

        & img:hover {
          transform: scale(1.1);
          box-shadow: 0 3px 5px black;
        }


        & p {
          height: 50%;
          overflow-y: auto;
        }
      }
    }

  h6 {
    color: $yellow;
  }

  div._btn {
    text-align: center;
    margin-top: 80px;
  }
  
  #articles #left > #imgBig > ._col {
    width: 100%;
  }

  #imgBig {
    --bs-gutter-x: 0;
  }
</style>
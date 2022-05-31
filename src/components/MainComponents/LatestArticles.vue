<template>
  <section id="3">
    <div class="container60">
      <div class="container-fluid">
        <div class="row">

          <div class="col-12 d-flex flex-column align-items-center">
            <h3>latest articles</h3>
            <div class="line"></div>
            <span>Together we make all the difference</span>
          </div>

          <div id="articles" class="col-12 mt-5">
            <div class="row h-100">

              <div id="left" class="col-8 col-md-6">
                <img :src="articles[activeArticleIndex].imageBig" alt="">
                <div class="p-3">
                  <h6>{{articles[activeArticleIndex].title}}</h6>
                  <p>{{articles[activeArticleIndex].description}}</p>
                </div>
              </div>

              <div id="right" class="col-4 col-md-6">

                <div v-for="(article, index) in articles" 
                :key="index"
                @click="activeArticle(index)">

                  <img :src="article.imageLittle" alt="">

                  <div class="w-75 ps-2 d-none d-md-inline-block">
                    <h6>{{article.title}}</h6>
                    <p>{{article.description}}</p>
                  </div>

                </div>
              </div>
            </div>
          </div>

          <div class="_btn red">view all our articles</div>

        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'LatestArticles',

  data() {
    return {
      activeArticleIndex: 0,

      articles: [
        {
          title: 'Understanding community  complexities',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat quidem magni iure quos a. Eius.',
          imageBig: require('../../assets/images/../../assets/images/photo-1444213007800-cff19e1677ac-600x450.jpg'),
          imageLittle: require('../../assets/images/../../assets/images/photo-1444213007800-cff19e1677ac-200x150.jpg'),
        },
        {
          title: 'The uman story of uniqueness',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat quidem magni iure quos a. Eius.',
          imageBig: require('../../assets/images/photo-1444664597500-035db93e2323-177x142.jpg'),
          imageLittle: require('../../assets/images/photo-1444664597500-035db93e2323-177x142.jpg'),
        },
        {
          title: 'Sustainable trade tactics',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat quidem magni iure quos a. Eius.',
          imageBig: require('../../assets/images/photo-1447430617419-95715602278e-177x142.jpg'),
          imageLittle: require('../../assets/images/photo-1447430617419-95715602278e-177x142.jpg'),
        },
        {
          title: 'Farmers making a difference',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat quidem magni iure quos a. Eius.',
          imageBig: require('../../assets/images/photo-1460230525622-630fe3294cd7-177x142.jpg'),
          imageLittle: require('../../assets/images/photo-1460230525622-630fe3294cd7-177x142.jpg'),
        },
        {
          title: 'Meeting remote tribes in Peru',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat quidem magni iure quos a. Eius.',
          imageBig: require('../../assets/images/photo-1460600421604-5e138c208b9c-177x142.jpg'),
          imageLittle: require('../../assets/images/photo-1460600421604-5e138c208b9c-177x142.jpg'),
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

  #articles::after {
    content: "";
    display: table;
    clear: both;
  }

  #articles {
    height: 55vh;
  }

  #left {
      float: left;
      height: 100%;
      overflow-y: auto;
      padding: 0;

      & > div {
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
      float: right;
      height: 100%;
      overflow-y: auto;
      cursor: pointer;
      padding: 0 0 0 20px;

      & > div {
        height: 25%;
        overflow-y: auto;
        padding-bottom: 15px;
        display: flex;

        & > div {
          height: 100%;
          overflow-y: auto;
        }

        & img {
          height: fit-content;
          width: 120px;
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
  
</style>
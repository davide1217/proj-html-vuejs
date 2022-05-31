<template>
  <section id="1">
    <div class="container-fluid h-100">
      <div class="row h-100">
        <div class="d-none d-sm-flex col-6 col-lg-8 left">
          <div>
            <h3>every moment counts</h3>
            <div class="line"></div>
            <div id="text" class="mb-2">
              <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Iusto labore aliquid non saepe ut vitae facere illo alias ipsam pariatur ea impedit reprehenderit hic sequi doloremque magnam distinctio.</p>
              <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ex commodi veritatis corporis, incidunt at eius ea quo! Reiciendis corporis labore quas, dolor voluptatum facilis id, voluptas commodi magnam, error perferendis.</p>
              <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Assumenda nam perspiciatis ex sit consequuntur itaque.</p>
            </div>
            <a href="#" class="_btn full">our mission</a>
          </div>
        </div>

        <div class="col-12 col-sm-6 col-lg-4 right">
          <div>
            <span><i class="fa-regular fa-heart"></i> 2032</span> 
            <div>Volunteers worldwide</div>
          </div>

          <div>
            <span><i class="fa-solid fa-globe"></i> 132</span>
            <div>Active projects</div>
          </div>

          <div>
            <span><i class="fa-solid fa-dollar-sign"></i> 3.8 M</span>
            <div>Donated</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MomentCounts',
}
</script>

<style lang="scss" scoped>
@import '../../assets/styles/_mixins';

  section {
    height: 55vh;

    & > div {
      overflow-y: auto;
    }
  }

  .left {
    height: 100%;
    padding: 60px 0;
    @include flex;

    & > div {
      width: 80%;
      height: 100%;
    }
    
    & h3 {
      color: black;
    }
  }

  #text {
    height: 50%;
    overflow-y: auto;

    & > p {
      margin-bottom: 10px;
    }
  }

  .right {
    height: 100%;
    background-image: url(../../assets/images/home-content-bg-1.jpg);
    background-size: cover;
    background-position: center;
    @include flex-column;
    justify-content: center;

    & > div {
      text-align: center;
      margin-bottom: 30px;

      & > span {
        font-size: 2rem;
      }
    }
  }
</style>
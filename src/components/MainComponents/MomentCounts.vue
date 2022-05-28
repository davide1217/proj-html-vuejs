<template>
  <section>
    <div class="left h-100">
      <div class="h-75">
        <h3>every moment counts</h3>
        <div class="line"></div>
        <div id="text" class="mb-4">
          <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Iusto labore aliquid non saepe ut vitae facere illo alias ipsam pariatur ea impedit reprehenderit hic sequi doloremque magnam distinctio.</p>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ex commodi veritatis corporis, incidunt at eius ea quo! Reiciendis corporis labore quas, dolor voluptatum facilis id, voluptas commodi magnam, error perferendis.</p>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Assumenda nam perspiciatis ex sit consequuntur itaque.</p>
        </div>
        <a href="#" class="_btn full">our mission</a>
      </div>
    </div>

    <div class="right d-flex flex-column align-items-center justify-content-center">
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
  </section>
</template>

<script>
export default {
  name: 'MomentCounts',
}
</script>

<style lang="scss" scoped>

  section {
    height: 50vh;
  }

  .left {
    float: left;
    width: 70%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;

    & > div {
      width: 80%;
    }
    
    & h3 {
      color: black;
    }
  }

  #text {
    height: 55%;
    overflow-y: auto;
  }

  .right {
    float: right;
    width: 30%;
    height: 100%;
    background-image: url(../../assets/images/home-content-bg-1.jpg);
    background-size: cover;
    background-position: center;

    & > div {
      text-align: center;
      margin-bottom: 30px;

      & > span {
        font-size: 2rem;
      }
    }
  }
</style>
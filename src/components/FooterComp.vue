<template>
  <footer>
    <section>
      <img src="../assets/images/avada-charity-sticky-header-logo.png" alt="">
    </section>

    <section>
      <div class="mb-3 text-center">
        <span>&copy; Copyright 2012 <span class="text-uppercase"><span>2020 avada theme by theme fusion</span> | <span>all rights reserved</span> | <span>powered by wordpress</span></span></span>
      </div>

      <div>
        <FooterMenu v-for="(icon, index) in icons"
        :key="`icon-${index}`"
        :icon="icon" />
      </div>

    </section>
  </footer>
</template>

<script>
import FooterMenu from './ExtraComp/FooterMenu'
export default {
  components: { FooterMenu },
  name: 'FooterComp',

  data() {
    return {
      icons: ['facebook-f', 'instagram', 'twitter', 'youtube'],
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/styles/_vars';
@import '../assets/styles/_mixins';

section {
    height: 15vh;
}

section:first-child {
  display: flex;
  justify-content: center;
  align-items: center;
}

section:last-child{
  background-color: #F5F5F5;
  @include flex-column;
  justify-content: center;

   & > div {
    & span {
      margin: 0 5px;
      color: $light-grey;
      font-size: .7rem;
    }

    & > i {
      color: $yellow;
      font-size: 1.3rem;
      border-radius: 50%;
      background-color: white;
    }
   }

   #facebook-f {
     padding: 9px 13px;
   }

   #instagram {
     padding: 9px 11px;
   }

   #twitter {
     padding: 9px;
   }

   #youtube {
     padding: 9px 8px;
   }
}
</style>
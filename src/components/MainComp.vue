<template>
  <main>
    <MomentCounts />
    <OurValues />
    <RecentCauses />
    <div class="_btn red">view all our causes</div>
    <LatestArticles />
    <ChangeLife />
  </main>

</template>

<script>
import ChangeLife from './MainComponents/ChangeLife.vue'
import LatestArticles from './MainComponents/LatestArticles.vue'
import MomentCounts from './MainComponents/MomentCounts.vue'
import OurValues from './MainComponents/OurValues.vue'
import RecentCauses from './MainComponents/RecentCauses.vue'
export default {
  components: {
    MomentCounts,
    OurValues,
    RecentCauses,
    LatestArticles,
    ChangeLife, 
  },
  name: 'MainComp'
}
</script>

<style lang="scss" scoped>
@import '../assets/styles/_vars';
@import '../assets/styles/_mixins';

div {
  height: 12vh;
  @include flex;
  font-size: .8rem;
}
</style>
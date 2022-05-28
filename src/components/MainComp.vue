<template>
  <main>
    <MomentCounts />
    <OurValues />
  </main>

</template>

<script>
import MomentCounts from './MainComponents/MomentCounts.vue'
import OurValues from './MainComponents/OurValues.vue'
export default {
  components: {
    MomentCounts,
    OurValues 
  },
  name: 'MainComp'
}
</script>

<style lang="scss" scoped>

</style>
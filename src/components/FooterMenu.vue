<template>
  <i :id="icon" class="fa-brands mx-2" :class="`fa-${icon}`"></i>
</template>

<script>
export default {
name: 'FooterMenu',

  props: {
    icon: String,
  }
}
</script>

<style lang="scss" scoped>

</style>
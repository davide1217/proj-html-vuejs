<template>
<li>
  <a class="text-uppercase" :class="{'_btn full' : index == menu.length - 1}" :href="`#${index}`">{{text}}</a>
</li>
</template>

<script>
export default {
  name: 'HeaderMenu',

  props: {
    text: String,
    index: Number,
    menu: Array
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/_vars';

  ul {
    list-style: none;

    & li {
      display: inline-block;
      margin: 10px;
      & a {
        font-size: .7rem;
        color: white;
      }

      & a:not(li:last-of-type a):hover {
        color: lighten($yellow, 20%);
      }

      & a:not(li:last-of-type a):focus {
        color: $yellow;
      }
    }
  }
</style>
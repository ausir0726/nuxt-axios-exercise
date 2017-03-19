<template lang="pug">
.container
  .row
    h1 FINPO nuxt starter
  .row
    ul
      li
        nuxt-link(to="/") Home
      li
        nuxt-link(to="/about") About
      li
        nuxt-link(to="/posts") Posts
  nuxt
  my-footer
</template>

<script>
import MyFooter from '~components/Footer.vue';

export default {
  components: {
    MyFooter,
  },
};
</script>

<style lang="stylus">

</style>

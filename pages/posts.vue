<template lang="pug">
section
  h1 all my posts
  ul
    li(v-for="data in results") 
      nuxt-link(:to="'/post/'+data.slug") {{data.title}}

</template>

<script>
import axios from 'axios';

export default {
  async data() {
    const { data } = await axios.get('https://cdn.upage.cool/f/pages/site/55a489ca4cfb0e11005f8f9d?category=55a4ab344cfb0e11005f8fbe&children=true&content=true&page=1');
    return data;
  },
  head() {
    return {
      title: 'sitename',
    };
  },
};
</script>

<style lang="stylus" scoped>

</style>

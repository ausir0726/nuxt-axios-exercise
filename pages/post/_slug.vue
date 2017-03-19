<template lang="pug">
section
  p
    nuxt-link(to="/posts") back to posts
  h1 post {{title}}
  img(:src="cover")
  p(v-html="content")

</template>

<script>
import axios from 'axios';

export default {
  async data({ params }) {
    const { data } = await axios.get(`https://cdn.upage.cool/f/pages/site/55a489ca4cfb0e11005f8f9d/slug/${params.slug}`);
    // console.log(data);
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
img
  width: 200px
p
  padding-top: 20px
</style>

<template>
  <div class="">
    <nuxt-link to="/posts/1" class="btn">Holi</nuxt-link>
    <nuxt-link to="/posts/2" class="btn">Holi</nuxt-link>
    <PostList :posts="loadedPosts"/>
  </div>
</template>

<script>
import PostList from '~/components/Posts/PostList.vue'

export default {
  components: {
    PostList
  },
  data() {
    return {
      loadedPosts: [
        {
          id: '1',
          title: "First Post",
          previewText: 'This is our post',
          thumbnail: 'https://d1bvpoagx8hqbg.cloudfront.net/originals/experiencia-erasmus-zaragoza-espana-marie-3ff9c03b590bf673030179f08c7e5dd4.jpg'
        }
      ]
    }
  }
}
</script>

<style>
.container
{
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.title
{
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
.subtitle
{
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}
.links
{
  padding-top: 15px;
}
</style>

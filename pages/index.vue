<template>
  <div class="">
    <input type="text" v-model="userID">
    <button @click="onLoadUser">Go to link</button>
    <nuxt-link to="/posts/1" class="btn">Holi</nuxt-link>
    <nuxt-link to="/posts/2" class="btn">Holi</nuxt-link>
    <PostList />
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import PostList from '~/components/Posts/PostList.vue'

export default {
  components: {
    Logo,
    PostList
  },
  data() {
    return {
      userID: ''
    }
  },
  methods: {
    onLoadUser() {
      this.$router.push('/posts/' + this.userID);
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

<template>
  <div class="admin-page">
    <section>
      <button @click="$router.push('/admin/new-post')">Create Post</button>
    </section>
    <section>
      <h2>Existing Posts</h2>
      <PostList isAdmin="true"/>
    </section>
  </div>
</template>

<script>
import PostList from '@/components/Posts/PostList'

export default {
  components: {
    PostList
  }
}
</script>

<style lang="css">
</style>

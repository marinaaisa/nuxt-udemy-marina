<template>
  <section>
    <PostPreview
    v-for="post in posts"
    :key="posts.id"
    :id="posts.id"
    :is-admin="isAdmin"
    :title="posts.title"
    :thumbnail="posts.thumbnail"
    :previewText="posts.previewText" />
  </section>
</template>

<script>
import PostPreview from '@/components/Posts/PostPreview'

export default {
  components: {
    PostPreview
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: false
    },
    posts: {
      type: Array,
      required: true
    }
  }
}
</script>

<style lang="css">
</style>

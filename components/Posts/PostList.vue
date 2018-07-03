<template>
  <section>
    <PostPreview
    v-for="post in posts"
    :key="post.id"
    :id="post.id"
    :is-admin="isAdmin"
    :title="post.title"
    :thumbnail="post.thumbnail"
    :previewText="post.previewText" />
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

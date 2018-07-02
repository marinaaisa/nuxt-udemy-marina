<template>
  <nuxt-link :to="postLink">
    <div :style="{ backgroundImage: 'url(' + thumbnail + ')' }" class="image">

    </div>
    <h1>{{ title }}</h1>
    <p>{{ previewText }}</p>
  </nuxt-link>
</template>

<script>
export default {
  name: 'PostPreview',
  props: {
    title: {
      type: String
    },
    isAdmin: {
      type: Boolean,
      required: false
    },
    id: {
      type: String
    },
    previewText: {
      type: String
    },
    thumbnail: {
      type: String
    }
  },
  computed: {
    postLink() {
      return this.isAdmin ? '/admin/' + this.id : '/posts/' + this.id
    }
  }
}
</script>

<style lang="css">
.image {
  height: 200px;
}
</style>

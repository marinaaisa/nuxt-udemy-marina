<template>
  <div>
    <AdminPostForm :post="loadedPost" />
  </div>
</template>

<script>
import AdminPostForm from '@/components/Admin/AdminPostForm'

export default {
  components: {
    AdminPostForm
  },
  data () {
    return {
      loadedPost: {
        author: 'Marina',
        title: 'Holi holi',
        content: 'super content',
        thumbnailLink: 'https://estaticos.elperiodico.com/resources/jpg/2/2/1516874504922.jpg'
      }
    }
  }
}
</script>

<style lang="css">
</style>

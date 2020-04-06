<template>
    <v-btn
        icon
        @click="deletePost(postId)"
        v-if="creatorId === authUser"
    >
    <v-icon>mdi-delete</v-icon>
    </v-btn>
</template>

<script>

export default {
  props: {
    token: String,
    postId: String,
    authUser: String,
    creatorId: String
  },
  methods: {
    deletePost (postId) {
      let vm = this
      let method = 'DELETE'
      let url = `http://localhost:3000/feed/post/${postId}`

      fetch(url, {
        method: method,
        headers: {
          Authorization: `Bearer ${vm.token}`
        }
      })
        .then(res => {

        })
        .catch(err => {
          console.log(err)
        })
    }
  }
}

</script>

<style scoped>

</style>

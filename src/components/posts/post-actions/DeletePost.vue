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
  }
}

</script>

<style scoped>

</style>

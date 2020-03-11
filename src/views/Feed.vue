<template>
  <div>
    <v-content>
      <v-spacer></v-spacer>
      <v-row class="d-flex justify-center">
        <v-col cols="12" xs="12" sm="12" md="3" lg="2" class="order-xs-3 order-sm-3 order-md-2 order-lg-1">
          <section>
            <!-- Left Column -->
            <h1>Recent Media</h1>
            <template v-if="posts.length != 0">
              <div v-for="post in posts" :key="post._id">
                {{ post._id }}
              </div>
            </template>
            <template v-else>
              <h1>Nothing to show.</h1>
            </template>
           </section>
        </v-col>
        <v-col cols="12" xs="12" md="7" sm="12" lg="5" class="order-xs-1 order-sm-1 order-md-1 order-lg-2">
          <!-- Middle column -->
          <v-btn @click="singlePostModal=true, newPost=true">new post</v-btn>
          <template v-if="posts">
            <v-card
            class="post"
            outlined
            tile
            ripple
            v-for="post in posts"
            :key="post._id">
              <SinglePost
                :authUser="authUser"
                :post="post"
                :token="token"
                @view="viewPost($event)"
                @delete="deletePost($event)"
              />
            </v-card>
          </template>
          <template v-else>
            <h1>You don't have anything in your feed.</h1>
          </template>
        </v-col>
        <v-col cols="12" xs="12" sm="12" md="12" lg="2" class="order-xs-2 order-sm-2 order-md-2 order-lg-3">
          <section>
          <!-- Right Column -->
          <h1>Recommended</h1>
          </section>
        </v-col>
      </v-row>
      <v-spacer></v-spacer>
    </v-content>
      <PostModal
        :dialog="this.singlePostModal"
        :fetchedPostData="this.fetchedPostData"
        :editMode="this.editMode"
        :viewMode="this.viewMode"
        :newPost="this.newPost"
        :authUser="this.authUser"
        @accept="savePost($event)"
        @edit="editMode=true; viewMode=false"
        @editedPost="updatePost($event)"
        @cancel="cancelModal()"
      />
    </div>
</template>

<script>
import PostModal from '../components/posts/PostModal'
import SinglePost from '../components/posts/SinglePost'

export default {
  props: {
    token: String,
    authUser: String
  },
  components: {
    SinglePost,
    PostModal
  },
  data: () => {
    return {
      posts: [],
      singlePostModal: false,
      fetchedPostData: {},
      editMode: false,
      viewMode: false,
      newPost: false,
      eventData: {}
    }
  }
}
</script>

<style scoped>
  .post {
    padding: 1rem;
  }
</style>

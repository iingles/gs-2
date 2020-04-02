<template>
    <div>
      <h1>feed</h1>
        <template v-if="posts">
            <b-card
                v-for="post in posts"
                :key="post.id"
            >
                <SinglePost
                  :id="post.id"
                />
            </b-card>
        </template>
        <template>
            <h1>Nothing in your feed.</h1>
        </template>
    </div>
</template>

<script>
import SinglePost from '../components/posts/SinglePost'

export default {
  components: { SinglePost },
  data: () => {
    return {
      posts: []
    }
  }
}
</script>

<style lang="less" scoped>

</style>

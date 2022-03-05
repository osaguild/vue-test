<template>
  <div :style="{fontSize: postFontSize + 'em'}">
    <blog-post v-for="(post,index) in posts" :key="index" :title="post.title" @enlarge-text="postFontSize += $event"></blog-post>
  </div>
</template>

<script>
import BlogPost from './components/BlogPost.vue'

export default {
  name: 'App',
  data() {
    return {
      posts: [
        { title: 'Vegetables' },
        { title: 'Cheese' },
        { title: 'Whatever else humans are supposed to eat' }
      ],
      postFontSize: 1
    }
  },
  components: {
    BlogPost
  }
}
</script>
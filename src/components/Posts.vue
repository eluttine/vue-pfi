<template>
  <div class="posts">
    <div class="w3-row-padding">
      <card v-for="post in posts" v-bind:post="post"></card>
    </div>
  </div>
</template>

<script>
import Card from './Card'

// var apiURL = 'http://localhost:9000/api/posts'

export default {
  name: 'posts',

  components: {
    Card
  },

  data () {
    return {
      posts: []
    }
  },

  created: function () {
    this.fetchPosts()
  },

  methods: {
    fetchPosts () {
      this.$http.get('http://localhost:8000/api/posts/').then((response) => {
        this.posts = response.data
      }, (response) => {
        console.log('API call error: ' + response.status + ': ' + response.statusText)
      })
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<!-- <style scoped>
</style> -->

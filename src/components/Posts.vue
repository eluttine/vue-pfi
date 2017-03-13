<template>
  <div class="posts">
    <div class="w3-row-padding w3-margin-bottom w3-center" v-for="i in rowCount">
      <div class="w3-quarter" v-for="post in postCountInRow(i)">
        <card v-bind:post="post"></card>
      </div>
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
      cardsPerRow: 4,
      posts: []
    }
  },

  created: function () {
    this.fetchPosts()
  },

  computed: {
    rowCount () {
      return Math.ceil(this.posts.length / this.cardsPerRow)
    }
  },

  methods: {
    fetchPosts () {
      this.$http.get('http://localhost:8000/api/posts/').then((response) => {
        this.posts = response.data
      }, (response) => {
        console.log('API call error: ' + response.status + ': ' + response.statusText)
      })
    },
    postCountInRow (index) {
      return this.posts.slice((index - 1) * this.cardsPerRow, index * this.cardsPerRow)
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<!-- <style scoped>
</style> -->

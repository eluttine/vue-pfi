
<template>
  <div class="card">
    <div class="card-image">
      <figure class="image is-400x300">
        <a v-bind:href="post.url" target="_blank">
          <img v-lazy="post.thumbnail">
        </a>
      </figure>
    </div>
    <div class="card-content">
      <div class="card-content">
        <small>{{ formatDate() }}</small>
        <p class="title is-5">
          <a v-bind:href="post.url" target="_blank">
            {{ post.title }}
          </a>
        </p>
        <p class="subtitle is-6">
          <a v-bind:href="post.feed.blog.url" target="_blank">
           <small>{{ post.feed.blog.title }}</small>
          </a>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import moment from 'moment'

export default {
  name: 'card',
  props: ['post'],

  computed: {
    authorList: function () {
      return this.post.authors.join(', ')
    }
  },

  methods: {
    formatDate () {
      moment.locale('fi')
      return moment(this.post.date_modified).format('LL')
    }
  }
}
</script>

<style>
a {
  color: black;
}
a:hover {
  color: gray;
}


.card {
  height: 100%;
  max-width: 400px;
  display: flex;
  flex-direction: column;
  margin: auto;
}

.card-content {
  padding: 10px;
}
</style>

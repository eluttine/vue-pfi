
<template>
  <div>
    <a v-bind:href="post.url" target="_blank">
      <img v-lazy="post.thumbnail" class="w3-hover-opacity post-image" />
    </a>
    <p>{{ formatDate() }}</p>
    <a v-bind:href="post.url" target="_blank">
      <h4>{{ post.title }}</h4>
    </a>
    <p>- {{ authorList }}</p>
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
.post-image {
  width: 100%;
}
</style>

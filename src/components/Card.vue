
<template>
  <div>
    <a v-bind:href="post.url" target="_blank">
      <img v-bind:src="post.thumbnail" style="width:100%">
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
body,h1,h2,h3,h4,h5,h6,p {font-family: "Karma", sans-serif}
</style>

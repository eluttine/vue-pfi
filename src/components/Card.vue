<template>
  <div class="w3-third">
    <div class="w3-card-5">
      <a v-bind:href="post.url">
        <img v-bind:src="post.thumbnail" alt="Norway" style="width:100%">
      </a>
      <header>
        <h2>{{ post.title }}</h2>
        <h4>{{ post.author }}</h4>
      </header>
      <div class="w3-container w3-center">
        <p>The Troll's tongue in Hardanger, Norway</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'card',
  props: ['post']
}
</script>

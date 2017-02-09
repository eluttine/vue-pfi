<template>
  <div id="app">
    <div class="w3-main w3-content w3-padding" style="max-width:1200px;margin-top:100px">
      <posts></posts>
    </div>
  </div>
</template>

<script>
import Posts from './components/Posts'

export default {
  name: 'app',
  components: {
    Posts
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

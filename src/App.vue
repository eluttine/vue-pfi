<template>
  <div id="app">
    <header class="w3-container w3-theme w3-padding">
      <div class="w3-center">
        <h1 class="w3-xxxlarge w3-animate-top">Purjehtijat.fi</h1>
        <h4>Tuulesta temmattua..</h4>
      </div>
    </header>
    <posts></posts>
    <footer class="w3-container w3-padding-32 w3-theme-d1 w3-center">
      <a class="w3-btn-floating w3-teal" href="https://twitter.com/purjehtijatFI" title="Twitter">
        <i class="fa fa-twitter"></i>
      </a>
    </footer>
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

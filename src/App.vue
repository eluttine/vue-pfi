<template>
  <div>

    <!-- Links on top -->
    <div class="w3-top w3-light-gray">
      <div class="w3-row w3-large">
        <div class="w3-col s3">
          <a href="#" class="w3-button w3-block">Purjehtijat.fi</a>
        </div>
        <div class="w3-col s3">
          <a href="#about" class="w3-button w3-block">About</a>
        </div>
      </div>
    </div>

    <!-- Content -->
    <div class="w3-content w3-padding content">

      <div class="w3-panel">
        <h1>Purjehtijat.fi</h1>
      </div>

      <!-- Posts -->
      <div class="w3-padding">
        <posts></posts>
      </div>

    </div>

    <!-- Footer -->
    <footer class="w3-container w3-padding-32 w3-light-grey w3-center">
      <a href="#app" class="w3-button w3-margin"><i class="fa fa-arrow-up w3-margin-right"></i>Alkuun</a>
      <div class="w3-xlarge w3-section">
        <i class="fa fa-instagram w3-hover-text-purple"></i>
        <i class="fa fa-twitter w3-hover-text-light-blue"></i>
        <i class="fa fa-github w3-hover-text-gray"></i>
      </div>
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
  margin-top: 60px;
}

.content {
  max-width: 1100px;
  margin-top: 80px;
  margin-bottom: 80px;
}
</style>

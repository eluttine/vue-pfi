<template>
  <div>
    <nav class="nav">
      <div class="nav-left">
        <a class="nav-item">
          <img src="http://bulma.io/images/bulma-logo.png" alt="Bulma logo">
        </a>
      </div>

      <!-- This "nav-menu" is hidden on mobile -->
      <!-- Add the modifier "is-active" to display it on mobile -->
      <div class="nav-right nav-menu">
        <span class="nav-item">
          <a class="button" >
            <span class="icon">
              <i class="fa fa-twitter"></i>
            </span>
            <span>Tweet</span>
          </a>
        </span>
      </div>
    </nav>

    <!-- Content -->
    <div class="section main pfi-grid">
      <posts></posts>
    </div>

    <foot></foot>
  </div>
</template>

<script>
import Posts from './components/Posts'
import Foot from './components/Footer'

export default {
  name: 'app',
  components: {
    Posts,
    Foot
  }
}
</script>

<style>
@import '../node_modules/bulma/css/bulma.css';

#app {
  margin-top: 60px;
}

.content {
  max-width: 1100px;
  margin-top: 80px;
  margin-bottom: 80px;
}
</style>

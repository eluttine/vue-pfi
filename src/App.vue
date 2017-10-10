<template>
  <div>
    <div class="hero-body">
      <div class="container has-text-centered">
        <h1 class="title is-1">
          Purjehtijat.fi
        </h1>
        <h2 class="subtitle is-5">
          Tuulesta temmattua.
        </h2>
      </div>
    </div>

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
  /* max-width: 1100px; */
  margin-top: 80px;
  margin-bottom: 80px;
}
</style>

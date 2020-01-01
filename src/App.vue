<template>
  <div id="app">
    <div class="container">
      <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
        <a class="navbar-brand" href="#">Mainankita</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
          <div class="navbar-nav">
            <a class="nav-item nav-link active" href="#">Home <span class="sr-only">(current)</span></a>
          </div>
        </div>
      </nav>
    </div>
    <HelloWorld/>
    <home/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import home from './views/home'

export default {
  name: 'app',
  components: {
    HelloWorld,
    home
  }
}
</script>

<style>
#app {
  
}
</style>

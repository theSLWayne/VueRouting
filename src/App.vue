<template>
  <div id="app">
    <Navbar />
    <div class="container">
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'

export default {
  name: 'App',
  components: {
    Navbar
  }
}
</script>

<style>
*{
  font-family: 'Roboto Slab', Helvetica, sans-serif;
}
body{
  background-color: #f5f3ef;
}
</style>

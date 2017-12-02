<template>
  <div id="wrap" class="wrapper">
    <nav class="navbar">
      <div class="container-fluid">
        <div class="navbar-header">
        </div>
      </div>
    </nav>
    <div id="main" class="container">
      <div id="app">
        <router-view/>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'app'
  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    font-size: 115%;
  }
</style>

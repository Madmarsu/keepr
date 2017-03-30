<template>
  <div id="app">
    <navbar></navbar>
    <router-view></router-view>
  </div>
</template>

<script>
  import Navbar from './components/NavBar'
  export default {
    name: 'app',
    components: {
      Navbar
    }
  }

</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
  }
  
  .input-field input[type=text]:focus+label {
    color: #1B4985;
  }
  
  .input-field input[type=text]:focus {
    border-bottom: 1px solid #1B4985;
    box-shadow: 0 1px 0 0 #1B4985;
  }
  
  .input-field input[type=password]:focus+label {
    color: #1B4985;
  }
  
  .input-field input[type=password]:focus {
    border-bottom: 1px solid #1B4985;
    box-shadow: 0 1px 0 0 #1B4985;
  }
</style>
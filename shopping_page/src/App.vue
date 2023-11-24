<template>
  <div class="container">
    <Navigation />
    <MainBody />
  </div>
</template>

<script>
 
  import MainBody from './components/MainBody.vue';
  import Navigation from './components/Navigation.vue';
  export default {
    name: 'App',
    components: {
      MainBody,
      Navigation
    }
    
  } 
</script>

<style>
#app {
  font-family: Lato;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
}
body{
  font-family: lato;
  color: #333;
  line-height: 1.6;
}
ul{
  list-style-type: none;
}
a{
  text-decoration: none;
  color: #333;

}
h1, h2{
    display: inline;
    float: left;
    font-weight: 300;
    line-height: 1.1;
    font-weight: bold;
}
</style>


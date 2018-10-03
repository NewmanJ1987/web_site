<template>
  <div id="app">
    <Header/>
  </div>
</template>

<script>
import Header from './components/Header.vue'

export default {
  name: 'app',
  components: {
    Header
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Mrs+Sheppards:400,700');
@import url('https://fonts.googleapis.com/css?family=Montserrat:400,700');

#app {
    height: calc(100% - 2em);
    font-family: 'Montserrat';
    font-size: 3em;
    color:white;
}
body, html {
    margin: 0;


}
</style>

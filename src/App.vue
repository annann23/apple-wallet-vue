<template>
  <div id="app">
    <Intro/>
    <!-- <card-1/> -->
  </div>
</template>

<script>
// import Card1 from './components/Card1.vue';
import Intro from './components/Intro.vue';

export default {
  components: { Intro },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #1d1d1f;
}

html, body{
  margin: 0;
  padding: 0;
}
</style>

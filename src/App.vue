<template>
  <div>
    <BackgroundMap/>
  </div>
</template>

<script>
import BackgroundMap from './components/BackgroundMap.vue';

export default {
  name: 'App',
  components: {
    BackgroundMap
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body {
  margin: 0px
}

</style>

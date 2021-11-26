<template>
  <div id="app">
    <Logo/>
    <Contenitorepadre />
  </div>
</template>

<script>
import Contenitorepadre from './components/Contenitorepadre.vue';
import Logo from './components/Logo.vue'

export default {
  name: 'App',
  components: {
    Contenitorepadre,
    Logo
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  
  
}
</style>

<template>
  <div id="app">
    <div id="contenitorelogo">
      <div class="spotylogo">
        <img
          id="spotylogo"
          src="../src\assets\logospoty.png"
          alt="logospotyfy"
        />
      </div>
      <Generimusic/>
    </div>
    <Contenitorepadre />
  </div>
</template>

<script>
import Contenitorepadre from "./components/Contenitorepadre.vue";
import Generimusic from "@/components/Selezionecanzoni.vue";
//import Logo from './components/Logo.vue'

export default {
  name: "App",
  components: {
    Contenitorepadre,
    //Logo
    Generimusic
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
#contenitorelogo {
  background-color: rgb(46, 58, 70);
  height: 100px;
  display: flex;
  align-items: center;
}
#spotylogo {
  width: 65px;
}
</style>

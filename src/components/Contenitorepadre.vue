<template>
 <div id="contenitorecard">
     <div class="centratura">
         <Cards/>
     </div>

 </div>
</template>

<script>
import Cards from '@/components/Cards.vue'

export default {
  name: 'Contenitorepadre',
  components: {
    Cards
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#contenitorecard{
    background-color: rgb(30, 45, 59);
    height: 600px;
}
.centratura{
    width: 80%;
    margin: 0 auto;
}
</style>

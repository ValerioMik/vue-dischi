<template>
 <select name="genre" id="" @change="$emit('search',$event)">
     <option :value="'tutto'">TUTTO</option>
     <option :value="'rock'">Rock</option>
     <option :value="'pop'">Pop</option>
     <option :value="'jazz'">Jazz</option>
      <option :value="'metal'">Metal</option>
 </select>
</template>

<script>
export default {
  name: 'Generimusic',
 
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
 select{
     width: 30%;
     margin-left: 970px;
     background-color: #2e3a46;
     color:#1ed760;
    
 }
</style>
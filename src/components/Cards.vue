<template>
 <div id="cards">
     <img :src="details.poster" alt="immagine">
     <h2>{{details.title}}</h2>
     <span><p>{{details.author}}</p></span>
     <span><p>{{details.year}}</p></span>
 </div>
</template>

<script>
export default {
  name: 'Cards',
  props:{
      details:Object,
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#cards{
    margin: 20px 10px 20px;
    background-color: rgb(46, 58, 70);
    height: auto;
    width: 14%;
    text-align: center;
    padding: 17px;
    
}
img{
    width: 100%;
}
h2 {
    color: white;  
}
p{
color: white; 
}
</style>







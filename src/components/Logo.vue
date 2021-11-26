<template>
 <div id="contenitorelogo">
    <div class="spotylogo"> 
        <img id="spotylogo" src="../../src\assets\logospoty.png" alt="logospotyfy">
    </div> 
 </div>
</template>

<script>
export default {
  name: 'Logo',
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#contenitorelogo{
    background-color: rgb(46, 58, 70);
    height: 100px;
    display: flex;
    align-items: center;
}
#spotylogo{
    width: 65px;
}
</style>

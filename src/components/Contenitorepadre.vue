<template>
  <div id="contenitorecard">
    <Generimusic @search="selectOption"/>
    <div class="centratura">
      <Cards
        v-for="(canzoni, i) in filtraDischi"
        :key="i"
        :details="canzoni"
      />
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Cards from "@/components/Cards.vue"
import Generimusic from "@/components/Selezionecanzoni.vue"

export default {
  name: "Contenitorepadre",
  components: {
    Cards,
    Generimusic
    
  },
  data() {
    return {
      apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
      listacanzoni: [],
      opzioneScelta: "tutto"
     
    };
  },
  created() {
    this.getcaracters();
  },
  methods: {
    getcaracters() {
      //console.log("ho finito una parte");
      axios.get(this.apiUrl).then((result) => {
        this.listacanzoni = result.data.response;
        //console.log(result.data);
      });
    },
   selectOption(event){
    this.opzioneScelta = event.target.value
   
  }, 
  },
  computed:{
    filtraDischi(){
      if(this.opzioneScelta === "tutto"){
        return this.listacanzoni
      }
      return this.listacanzoni.filter((item)=>{
        return item.genre.toLowerCase().includes(this.opzioneScelta.toLowerCase())
      })
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#contenitorecard {
  background-color: rgb(30, 45, 59);
  height: auto;
  padding: 50px;
}
.centratura {
  width: 70%;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
}
</style>

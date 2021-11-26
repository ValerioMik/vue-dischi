<template>
  <div id="contenitorecard">
    <div class="centratura">
      <Cards :v-for="canzoni,i in listacanzoni"
      :kei="i"
      :details="canzoni"/>
      
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Cards from "@/components/Cards.vue";

export default {
  name: "Contenitorepadre",
  components: {
    Cards,
  },
  data() {
    return {
      apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
      listacanzoni: [],
    };
  },
  created() {
    this.getcaracters();
  },
  methods: {
    getcaracters() {
      //console.log("ho finito una parte");
      axios
      .get(this.apiUrl)
      .then((result) => {
        this.listacanzoni = result.data
        //console.log(result.data);
      });
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#contenitorecard {
  background-color: rgb(30, 45, 59);
  height: 600px;
}
.centratura {
  width: 70%;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
</style>

<template>
  <main>

      <div class="container">

        <div class="row justify-content-center">
            
            <MyCard v-for="(cd, index) in listaCd" :key="index" :cd="cd"/>
            
        </div>

      </div>

  </main>
</template>

<script>
/*Integro Axios nel mio progetto*/
const axios = require('axios');
import MyCard from "./partials/MyCard.vue"

export default {
  name: "MyMain",
  components: {
    MyCard,
  },
  data() {
    return {
      listaCd : []
    }
  },
  methods: {
    getAlbums() {
        
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
          this.listaCd = response.data.response;
          console.log(response)
        })
        .catch(function (error) {
       
          console.log(error);
        })
        .then(function () {
     
        });
    }
  },
  mounted() {
    this.getAlbums();
  }
}
</script>

<style lang="scss" scoped>

 @import "src/assets/style/variables.scss";

   main {
       height: 100vh;
       background-color: $MainColor;

       .row{
         width: 80%;
         margin: auto;
       }
    
   }

</style>

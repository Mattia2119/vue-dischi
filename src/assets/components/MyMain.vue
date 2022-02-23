<template>
  <main>
   <div class="container">
  <div class="row align-items-start">
    <div class="col">
      
    </div>
    <div class="col">
      
    </div>
    <div class="col">
      
    </div>
    <div class="col">
      
    </div>
    <div class="col">
      
    </div>
  </div>
  <div class="row align-items-center">
    <div class="col">
      
    </div>
    <div class="col">
      
    </div>
    <div class="col">
      
    </div>
    <div class="col">
      
    </div>
    <div class="col">
      
    </div>
  </div>
  <div class="row align-items-end">
    <div class="col">
      
    </div>
    <div class="col">
      
    </div>
    <div class="col">
      
    </div>
    <div class="col">
      
    </div>
    <div class="col">
      
    </div>
  </div>
</div>
  </main>
</template>

<script>
/*Integro Axios nel mio progetto*/
const axios = require('axios');

export default {
  name: "MyMain",
  data() {
    return {
      listaCd : []
    }
  },
  methods: {
    getAlbums() {
        // Make a request for a user with a given ID
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
          this.listaCd = response.data;
          console.log(response)
        })
        .catch(function (error) {
        // handle error
          console.log(error);
        })
        .then(function () {
        // always executed
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
       height: calc(100vh - 60px);
       background-color: $MainColor;
       .col {
         height: 195px;
         margin: 11.4px;
         background-color: $HeaderColor;
       }
   }

</style>

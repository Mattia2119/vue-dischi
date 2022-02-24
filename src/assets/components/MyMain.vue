<template>
  <main>

      <div class="container">

        <div class="row gx-4 justify-content-center">

            <div class="col-lg-2 col-md-12 personal" v-for="(cd, index) in listaCd" :key="index">
              <img :src="cd.poster">
              <h3>{{cd.title}}</h3>
              <p>{{cd.author}}</p>
              <p>{{cd.year}}</p>
            </div>

        </div>

        <!--Seconda Row-->

        <div class="row gx-4 justify-content-center">

            <div class="col-lg-2 col-md-12 personal">

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
        
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
          this.listaCd = response.data;
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
       height: calc(100vh - 60px);
       background-color: $MainColor;
       display: flex;
       align-items: center;

       .personal{
         background-color: $HeaderColor;
         height: 250px;
         width: 150px;
         margin: 20px 15px;
         display: flex;
         align-items: center;
         flex-direction: column;
           img {
             height: 120px;
             margin-top: 15px;
           }
           h3 {
             color: white;
             font-size: 16px;
             margin-top: 10px;
           }
           p {
             font-size: 12px;
             color: lightgrey;
             font-weight: 600;
           }
       }
   }

</style>

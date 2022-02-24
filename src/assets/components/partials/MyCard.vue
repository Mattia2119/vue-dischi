<template>

    <div class="col-lg-2 col-md-6 personal">
        <img :src="cd.poster">
        <h3>{{cd.title}}</h3>
        <p>{{cd.author}}</p>
        <p>{{cd.year}}</p>
    </div>

</template>


<script>
export default {
    name: "MyCard",
    props: {
        cd: Object
    }
}
</script>


<style lang="scss" scoped>

@import "src/assets/style/variables.scss";

.personal{
         background-color: $HeaderColor;
         height: 250px;
         width: 150px;
         margin: 20px 15px;
         display: flex;
         align-items: center;
         flex-direction: column;
            img {
              height: 130px;
              margin-top: 10px;
            }

           h3 {
             color: white;
             font-size: 16px;
             margin-top: 10px;
           }
           p {
             margin-bottom: 0;
             font-size: 12px;
             color: lightgrey;
             font-weight: 600;
           }
       }
  
</style>


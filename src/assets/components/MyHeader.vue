<template>
    <header>
        <img src="../img/spotify-logo-png-7053.png" alt="Spotify-logo">
        <h3>{{thanks}}</h3>
    </header>
</template>

<script>
export default {
name: "MyHeader",
props: {
    "thanks": String
}

}
</script>

<style lang="scss" scoped>

 @import "src/assets/style/variables.scss";

   header {
       height: 60px;
       background-color: $HeaderColor;
       display: flex;
       align-items: center;
         img {
             height: 40px;
             margin-left: 20px;
             padding-right: 10px;
         }
         h3 {
             font-size: 14px;
             margin: 0;
             color: white;
         }

   }

</style>


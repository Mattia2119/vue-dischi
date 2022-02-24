<template>
  <div id="app">
    <MyHeader thanks="Boolean"></MyHeader>
    <MyMain>
      <MyCard/>
    </MyMain>
  </div>
</template>

<script>
import MyHeader from '../src/assets/components/MyHeader.vue'
import MyMain from '../src/assets/components/MyMain.vue'
import MyCard from '../src/assets/components/partials/MyCard.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
    MyCard,
  }
}
</script>

<style lang="scss">
 @import "src/assets/style/general.scss";
</style>

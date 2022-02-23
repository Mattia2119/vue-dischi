<template>
  <div id="app">
    <MyHeader thanks="Boolean"></MyHeader>
    <MyMain></MyMain>
  </div>
</template>

<script>
import MyHeader from '../src/assets/components/MyHeader.vue'
import MyMain from '../src/assets/components/MyMain.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
  }
}
</script>

<style lang="scss">
 @import "src/assets/style/general.scss";
</style>

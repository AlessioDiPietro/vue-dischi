<template>
  <div id="app">
    <Header/>

    <!-- corpo pagina -->
    <MainContent/>
    
  </div>
</template>

<script>
import Header from './components/Header.vue'
import MainContent from './components/MainContent.vue'

export default {
  name: 'App',
  components: {
    Header,
    MainContent
  },
}
</script>

<style lang="scss">
@import "@/assets/style/commons.scss";

body {
  background-color: $bgcSpot;
}

</style>

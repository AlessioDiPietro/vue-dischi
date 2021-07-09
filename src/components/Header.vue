<template>
  <nav class="d-flex justify-content-between">
      <img src="https://upload.wikimedia.org/wikipedia/commons/7/71/Spotify.png" alt="#">
      <SearchBar/>
  </nav>
</template>

<script>
import SearchBar from "@/components/SearchBar.vue"
export default {
    name: "header",
    components:{
        SearchBar,
    }

}
</script>

<style lang="scss" >
@import "@/assets/style/commons.scss";

    nav {
        background-color: $bgcSpotLight;
        height: 70px;
        padding: 12px 3px;
        img {
            height:100%;
        }
    }

</style>
<template>
  <nav>
      <img src="https://upload.wikimedia.org/wikipedia/commons/7/71/Spotify.png" alt="#">
  </nav>
</template>

<script>
export default {
    name: "header"

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
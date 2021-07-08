<template>
  <div class="card">
      <img :src="info.poster" :alt="info.title">

  </div>
</template>

<script>
export default {
    name: "MusicCard",
    props: ["info"]
}
</script>

<style lang="scss" scoped>
@import "@/assets/style/commons.scss";
    .card {
        background-color: $bgcSpotLight;
        width: 100%;
        height: 360px;
    }


</style>


// "poster": "https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg",
//             "title": "New Jersey",
//             "author": "Bon Jovi",
//             "genre": "Rock",
//             "year": "1988"
// ciao
<template>
  <div class="card">
      <img :src="info.poster" :alt="info.title">
      <h3>{{info.title}}</h3>

      <div class="sub-info">
          <h5>{{info.author}}</h5>
          <h6>{{info.year}}</h6>
      </div>

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
        height: 460px;
        padding: 15px;
        color: white;

        h3 {
            font-weight: bolder;
            margin: 15px;
        }
        .sub-info {
            color: grey;
            font-size: 15px;
        }
    }


</style>


// "poster": "https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg",
//             "title": "New Jersey",
//             "author": "Bon Jovi",
//             "genre": "Rock",
//             "year": "1988"
// ciao
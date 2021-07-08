<template>
  <div class="load-box">
      <h1>Caricamento..</h1>
  </div>
</template>

<script>
export default {
    name:"LoadingView"

}
</script>

<style lang="scss" scoped>
    .load-box{
        background-color: #fff;background: rgb(249,255,249);
        background: radial-gradient(circle, rgba(249,255,249,1) 0%, rgba(84,193,130,1) 21%, rgba(82,179,173,1) 74%, rgba(21,137,201,1) 100%);
        width: 100%;
        height: 82vh;
        position: relative;
        h1{
            font-size: 80px;
            color: rgb(114, 113, 113);
            top: 50%;
            left: 50%;
            position: absolute;
            transform: translate(-50%, -50%);
            
        }
    }

</style>
<template>
  <div class="search_bar m-5 d-flex justify-content-end align-items-center">
    <h2>Select Kind: </h2>
    <select class="form-select mx-3" aria-label="Default select example" selected v-model="key" @change="$emit('kind', key)">
        <option value="Pop">Pop</option>
        <option value="Jazz">jazz</option>
        <option value="Metal">Metal</option>
        <option value="Rock">Rock</option>
    </select>
  </div>
</template>

<script>
export default {
    name: "SearchBar",
    data(){
        return {
             key:"",
        }
    }


}
</script>

<style lang="scss" scoped>
    select {
        width: 100px;
        background-color: rgba(255, 255, 255, 0.267);
        color: rgb(144, 106, 106);
    }
    h2 {
        font-size:20px;
        color: rgb(144, 106, 106);
        margin-bottom: 0 ;
        
    }


</style>
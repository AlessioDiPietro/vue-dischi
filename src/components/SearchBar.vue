<template>
  <div class="search_bar mx-5 w-25">
    <select class="form-select w-25" aria-label="Default select example" selected v-model="key" @change="$emit('kind', key)">
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


</style>
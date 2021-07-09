<template>
  <div class="search_bar mx-5">
    <select class="form-select" aria-label="Default select example" selected v-model="selectedGen" @change="changing()">
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
             selectedGen: "",
        }
    },
    methods: {
        changing(){
            console.log(this.selectedGen)
            
        }
    }
    

}
</script>

<style lang="scss" scoped>


</style>
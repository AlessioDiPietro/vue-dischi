<template>
  <main>
      <div class="box p-5 text-center">
          <SearchBar @kind="filterKind"/>

        <div class="row d-flex justify-content-center" v-if="!loadStep">

            <div class="col-2 m-3" v-for="(item, index) in filterReturn" :key="index">

            <MusicCard :info="item" />

            </div>


        </div>
        
        <LoadingView v-else/>

      </div>
  </main>
</template>

<script>
import axios from 'axios'
import MusicCard from '@/components/MusicCard.vue'
import LoadingView from '@/components/LoadingView.vue'
import SearchBar from "@/components/SearchBar.vue"
export default {
    name: "MainContent",
    components:{
        MusicCard,
        LoadingView,
        SearchBar
    },
    data(){
        return{
            musicItems : "https://flynn.boolean.careers/exercises/api/array/music",
            dataMusic: "",
            loadStep: true,
            selecKind: ""
            
        }
    },
    created(){
        this.getDataApi()
        
    },
    methods: {
        getDataApi(){
            axios
                .get(this.musicItems)
                .then(result =>{
                    this.dataMusic= result.data.response
                    this.loadStep=false;
            })
        },
        filterKind(filterInput){
            this.selecKind = filterInput;

        }
        
    },
    computed: {
        filterReturn(){
            return this.dataMusic.filter(element => {
                return element.genre.includes(this.selecKind)
            })
        }
    }
}
</script>
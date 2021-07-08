<template>
  <main>
      <div class="box p-5 text-center">

        <div class="row d-flex justify-content-center" v-if="!loadStep">

            <div class="col-2 m-3" v-for="(item, index) in dataMusic" :key="index">

            <MusicCard :info="item"/>

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
export default {
    name: "MainContent",
    components:{
        MusicCard,
        LoadingView
    },
    data(){
        return{
            musicItems : "https://flynn.boolean.careers/exercises/api/array/music",
            dataMusic: "",
            loadStep: true
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
        }
    }
}
</script>
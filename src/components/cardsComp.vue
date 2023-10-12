<script>
import axios from 'axios';
import { store } from '../data/store.js'
import SingleCardComp from './SingleCardComp.vue'
export default {
  name: 'cardsComp',
  components:{
    SingleCardComp
  },
  data(){
    return{
      store,
      apiLimit: '?num=20&offset=0'
    }
  },
  methods:{
    getApi(){
      axios.get(store.apiUrl+this.apiLimit)
        .then( (resp) => {
          store.arrayCards = resp.data.data;
          
        } )
    }
  },
  mounted(){
    this.getApi()
    console.log(store.arrayCards);
  }
}
</script>

<template>
  <div class="d-flex flex-wrap bg-white">
    <SingleCardComp
      v-for="card in store.arrayCards"
      :key="card.id"
      :cardPropriety="card"/>
  
  

  </div>
</template>

<style lang="scss" scoped>

</style>
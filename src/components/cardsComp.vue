<script>
import axios from 'axios';
import { store } from '../data/store.js'
export default {
  name: 'cardsComp',
  data(){
    return{
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
  <div v-for="card in arrayCards" :key="card.id">{{ card }}</div>
</template>

<style lang="scss" scoped>

</style>
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
        .then( (card) => {
          store.arrayCards.push(card.data)

        } )
    }
  },
  mounted(){
    this.getApi()
  console.log(store.apiUrl+this.apiLimit);
  console.log(store.arrayCards);
  }
}
</script>

<template>
  <div></div>
</template>

<style lang="scss" scoped>

</style>
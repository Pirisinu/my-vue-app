<script>
import { store } from '../data/store.js'
import SingleCardComp from './SingleCardComp.vue'
export default {
  name: 'CardsComp',
  components:{
    SingleCardComp
  },
  data(){
    return{
      store
    }
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
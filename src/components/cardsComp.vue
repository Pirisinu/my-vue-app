<script>
import { store } from '../data/store.js'
export default {
  name: 'cardsComp',
  data(){
    return{
      
    }
  },
  mounted(){
    console.log(store.apiUrl);
  }
}
</script>

<template>
  <p>Cards</p>
</template>

<style lang="scss" scoped>

</style>
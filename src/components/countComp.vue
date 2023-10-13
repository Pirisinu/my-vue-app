<script>
import { store } from '../data/store';

export default {
  name: 'CountComp',
  data(){
    return{
      store
    }
  }
}
</script>

<template>
  <p>Found {{  store.arrayCards.length }} Cards</p>
</template>


<style lang="scss" scoped>

@use '../scss/partials/_vars.sass' as *;

p{
background-color:$fake-black;
color: white;
font-size: 1.4rem;
padding: 15px
}
</style>
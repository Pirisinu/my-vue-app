  
<script>

import selectComp from './selectComp.vue';
import countComp from './countComp.vue';
import cardsComp from './cardsComp.vue';

export default {
  name: 'mainComp',
  components:{
    selectComp,
    countComp,
    cardsComp
  }
}
</script>

<template>
  <main>
    <selectComp />
    <countComp />
    <cardsComp />


  </main>
</template>

<style lang="scss" >
@use '../scss/partials/_vars.sass' as *;

main{
background-color: $orange;
}
</style>
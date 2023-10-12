  
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

    <div class="my_container">
      <countComp />
      <cardsComp />
    </div>

  </main>
</template>

<style lang="scss" scoped>
@use '../scss/partials/_vars.sass' as *;

main{
background-color: $orange;
padding: 10px 30px;
.my_container{
  background-color: white;
}
}
</style>
  
<script>

import SelectComp from './SelectComp.vue';
import CountComp from './CountComp.vue';
import CardsComp from './CardsComp.vue';

export default {
  name: 'MainComp',
  components:{
    SelectComp,
    CountComp,
    CardsComp
  }
}
</script>

<template>
  <main>
    <SelectComp />

    <div class="my_container">
      <CountComp />

      <CardsComp />
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
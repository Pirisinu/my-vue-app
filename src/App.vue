
<script>

import headerComp from './components/headerComp.vue'
import mainComp from './components/mainComp.vue'


export default {
  name: 'App',
  components: {
    headerComp,
    mainComp
  }
}
</script>

<template>

  <headerComp />
  <mainComp />
  
</template>

<style lang="scss">

@use './scss/main.scss';

</style>

<script>

import axios from 'axios';
import { store } from '../data/store';


export default {
  name: 'SelectComp',
  data(){
    return{
      store,
      archetypeSel: []
    }
  },
  created(){
    axios.get(store.apiUrlArchtype)
    .then( (res) => {
      this.archetypeSel.push(...res.data)
    } )
    .catch( (err) => {
      console.log(err);
    });
  },
  methods:{
    archetypeSelChange(){
      axios.get(store.apiUrl+ '?archetype=' + this.store.archetypeSel)
      .then( (res) => {
        const cardSel = res.data.data
        this.store.arrayCards = cardSel;
      })
      .catch( (err) => {
        console.log(err);
      });
    }
  }
}
</script>
<template>
  <select 
  class="form-select" 
  aria-label="Default service example" 
  v-model="this.store.archetypeSel"
  @change="archetypeSelChange"
  >
    <option selected value="">Select Archetype</option>
    <option 
    v-for="archetype in archetypeSel"
    :key='archetype.id'
    :value="archetype.archetype_name"
    >
    {{ archetype.archetype_name }}
    </option>

  </select>
</template>

<style lang="scss" scoped>

</style>
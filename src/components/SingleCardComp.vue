<script>
export default {
 name: 'SingleCardComp',
 props: ['cardPropriety']
}
</script>


<template>
  <div class="card my-3 border-0">
        <img :src="cardPropriety.card_images[0].image_url" :alt="cardPropriety.name">
        <h4 class="fw-bold p-2">{{ cardPropriety.name }}</h4>
        <h5 class="p-2">{{ cardPropriety.archetype }}</h5>
    </div>
</template>


<style lang="scss" scoped>
@use '../scss/partials/_vars.sass' as *;

  .card {
    width: calc(100% / 5 - 20px);
    margin: 0 10px;
    background-color: $orange;
    &:hover{
      scale: 1.05;
    }
    h4,h5{
      text-align: center;
      color: white;
    }
}
</style>
<script>
export default {
 name: 'SingleCardComp',
 props: ['cardPropriety']
}
</script>


<template>
  <div class="card my-3 border-0">
        <img :src="cardPropriety.card_images[0].image_url" :alt="cardPropriety.name">
        <h4 class="text-center fw-bold text-white p-2">{{ cardPropriety.name }}</h4>
        <h5 class="text-center text-white p-2">{{ cardPropriety.archetype }}</h5>
    </div>
</template>


<style lang="scss" scoped>
@use '../scss/partials/_vars.sass' as *;

  .card {
    width: calc(100% / 5 - 20px);
    margin: 0 10px;
    background-color: $orange;
}
</style>
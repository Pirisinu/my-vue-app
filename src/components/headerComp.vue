  
<script>
export default {
  name: 'HeaderComp',
  props: ['cardPropriety']
}
</script>

<template>
  <header>
    <div class="logo-head">
      <img src="/public/Yu-Gi-Oh!_(Logo).jpg" alt="IMG">
    </div>
    <h1>Yu-Gi-OH Api</h1>
  </header>
</template>

<style lang="scss" scoped>

header{
  display: flex;
  padding: 15px; 
  height: 90px;
  div,h1{
    display: flex;
    align-items: center;
  }
  div{
    margin: 0px 10px;
    width: 150px;
    height: 50px;
    img{
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }
  h1{
    font-weight:600;

  }
}

</style>
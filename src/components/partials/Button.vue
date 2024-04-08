<script>
  export default {
    props:{
      link: String,
      content: String
    }
  }
</script>



<template>

  <button class="main-button btn text-uppercase rounded-5 border-0">
    <a :href="link" >{{ content }}</a>
  </button>

</template>



<style lang="scss" scoped>

@use '../../assets/scss/partials/vars' as *;

  .main-button{
    width: 160px;
    height: 50px;
    font-size: .9rem !important;
    background: $gradient-green-toleft;
    box-shadow: 10px 5px 20px 1px lighten( $text-cyan, 30%);
    transition: all .3s;
    a{
      text-decoration: none !important;
      color: $fill-white !important;
    }
    &:hover{
      background: $gradient-black;
      box-shadow: 10px 5px 20px 1px lighten( $bg-black, 40%);
    }
  }

</style>
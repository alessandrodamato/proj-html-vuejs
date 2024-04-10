<script>
  export default {
    props:{
      link: String,
      content: String
    }
  }
</script>



<template>

  <button class="main-button btn text-uppercase rounded-5 border-0 p-0 overflow-hidden">
    <a class="d-inline-block w-100 h-100" :href="link" >{{ content }}</a>
  </button>

</template>



<style lang="scss" scoped>

@use '../../assets/scss/partials/vars' as *;

  .main-button{
    width: 160px;
    height: 50px;
    font-size: .9rem !important;
    @include gradient(left, $bg-green, #96e060);
    box-shadow: 10px 5px 20px 1px lighten( $text-cyan, 30%);
    transition: all .3s;
    a{
      line-height: 50px;
      text-decoration: none !important;
      color: $fill-white !important;
    }
    &:hover, &.dark{
      @include gradient(left, $fill-black, $gray-6);
      box-shadow: 10px 5px 20px 1px lighten( $bg-black, 40%);
    }
  }

</style>
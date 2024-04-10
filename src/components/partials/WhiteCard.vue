<script>
  export default {
    props:{
      iconClass: String,
      title: String,
      bio: String
    }
  }
</script>



<template>

  <div class="card rounded-4 border-0 mb-5">

    <div class="icon mb-4">
      <i :class="iconClass"></i>
    </div>

    <h3 class="mb-3">{{ title }}</h3>

    <p class="pe-4">{{ bio }}</p>

  </div>

</template>



<style lang="scss" scoped>

@use '../../assets/scss/partials/vars' as *;

  .card{
    &:hover{
      @include gradient(top right, $bg-green, #96e060);
      box-shadow: 0 0 15px 1px $bg-green;
      scale: 1.1;
      .icon i, h3, p{
        color: $fill-white;
      }
    }
    width: 450px;
    height: 320px;
    padding: 60px 40px;
    margin-left: 40px;
    box-shadow: 0 0 20px 5px $lg-3;
    background-color: white;
    .icon i{
      color: $text-green;
      font-size: 4rem;
    }
  }

</style>
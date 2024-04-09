<script>
  export default {
    props:{
      title: String,
      subtitle: String,
      price: String,
      type: String,
      features: String
    }
  }
</script>



<template>

  <div class="plan rounded-4 overflow-hidden">

    <div class="top mb-4"></div>

    <h4 class="text-uppercase text-center fw-bold">{{ title }}</h4>

    <p class="text-capitalize text-center mb-3">{{ subtitle }}</p>

    <div class="price text-center text-white mb-5">

      <span class="fs-2">$ </span>
      <span class="number">{{ price }}</span>
      <span class="fs-2 text-capitalize"> / {{ type }}</span>

    </div>

    <ul class="text-center">
      <li class="text-capitalize mb-4">creative design enabled</li>
      <li class="text-capitalize mb-4">vibrant color usage</li>
      <li class="text-capitalize mb-4">eye catching design</li>
      <li class="text-capitalize mb-4">extreme typography</li>
      <li class="text-capitalize mb-4">exceptional design</li>
    </ul>
    
  </div>

</template>



<style lang="scss" scoped>

@use '../../assets/scss/partials/vars' as *;

  .plan{
    &.theme-green .top, &.theme-green .price{
      @include gradient(left, $bg-green, #96e060);
    }
    &.theme-dark .top, &.theme-dark .price{
      @include gradient(left, $fill-black, $gray-6);
    }
    width: 333px;
    height: 570px;
    margin-left: 40px;
    flex-shrink: 0;
    box-shadow: 0 0 20px 5px $lg-3;
    .top{
      height: 20px;
    }
    .price{
      height: 125px;
      line-height: 125px;
      .number{
        font-size: 3.3rem;
      }
    }
    li::before{
      font-family: 'Font Awesome 5 Free';
      content: '\f00c';
      display: inline-block;
      padding-right: 10px;
      vertical-align: middle;
      font-weight: 900;
      color: $fill-black;
    }
  }

</style>
<script>
  export default {
    props:{
      name: String,
      category: String,
      path: String,
    }
  }
</script>



<template>
  
  <div class="card position-relative mb-1 border-0 text-white">
    <img :src="`/src/assets/img/${path}`" :alt="name" class="img-fluid">
    <div class="card-layer position-absolute top-0 start-0 w-100 h-100 p-5 d-none">
      <h4 class=" fw-bold">{{ name }}</h4>
      <span class="fs_09 text-uppercase">{{ category }}</span>
    </div>
  </div>

</template>



<style lang="scss" scoped>

@use '../../assets/scss/partials/vars' as *;

  .card{
    width: calc(100% / 4 - 4px);
    aspect-ratio: 1 / 1;
    overflow: hidden;
    &:hover{
      z-index: 1;
      scale: 1.1;
      .card-layer{
        @include gradient(bottom, rgba($bg-green, .8), rgba(#96e060, .8));
        display: flex !important;
        flex-direction: column;
        justify-content: flex-end;
      }
    }
  }

</style>
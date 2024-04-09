<script>
  export default {
    
  }
</script>



<template>

  <div>
    <div class="line sm mb-4"></div>
    <div class="line xl mb-4"></div>
  </div>
  
</template>



<style lang="scss" scoped>

@use '../../assets/scss/partials/vars' as *;

  .line{
    @include gradient(bottom, $bg-green, #96e060);
    display: inline-block;
    border-radius: 3px;
    height: 5px;
    &.sm{
      width: 10px;
    }
    &.xl{
      margin-left: 5px;
      width: 50px;
    }
  }

</style>
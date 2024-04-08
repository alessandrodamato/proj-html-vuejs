<script>
  export default {
    
  }
</script>



<template>

  <header>

    <div class="header-top">

      <div class="ad_container-sm container-fluid">
        
        <div class="row">

          <div class="col">a</div>
          <div class="col-auto">b</div>

        </div>

      </div>
      
    </div>

    <div class="header-bottom">

      <div class="ad_container-sm container-fluid">
        
        <div class="row row-cols-3">

          <div class="col">a</div>
          <div class="col">b</div>
          <div class="col">c</div>

        </div>

      </div>

    </div>

  </header>
  
</template>



<style lang="scss" scoped>

@use '../assets/scss/partials/vars' as *;

  header{

    .header-top{
      height: 40px;
      color: $fill-white;
      background: linear-gradient(to left, $gray-3, #3b3b3b);
    }

    .header-bottom{
      height: 105px;
    }

  }

</style>
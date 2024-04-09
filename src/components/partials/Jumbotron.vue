<script>
import DobuleLine from './DobuleLine.vue'
  export default {
    components:{
      DobuleLine
    } 
  }
</script>



<template>
  
  <section id="jumbotron">

    <div class="ad_container container-fluid h-100">
        
        <div class="row h-100">

          <div class="col-6 h-100">

            <h6 class="text-uppercase fw-bold">17 years of experience</h6>

            <h1 class="fw-bold">Focus on Your <span class="text-green">Business</span></h1>

          </div>

        </div>

      </div>

  </section>

</template>



<style lang="scss" scoped>

@use '../../assets/scss/partials/vars' as *;

  #jumbotron{
    height: 940px;
    padding: 160px 0 80px;
    background-color: $lg-1;
    background-image: url('../../assets/img/Group-35-2x.png');
    background-repeat: no-repeat;
    background-position: 175%;
    h6{
      @include gradient(bottom, $bg-green, #96e060);
      padding-left: 5px;
      letter-spacing: 10px;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent; 
      -moz-background-clip: text;
      -moz-text-fill-color: transparent;
    }
  }

</style>
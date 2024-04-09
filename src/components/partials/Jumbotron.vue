<script>
import DoubleLine from './DoubleLine.vue'
import Button from './Button.vue'
  export default {
    components:{
      DoubleLine,
      Button
    } 
  }
</script>



<template>
  
  <section id="jumbotron">

    <div class="ad_container container-fluid h-100">
        
        <div class="row h-100">

          <div class="col-6 h-100">

            <h6 class="years17 text-uppercase fw-bold">17 years of experience</h6>

            <h1 class="fw-bold mb-5">Focus on Your <span class="text-green">Business</span></h1>

            <DoubleLine class="mb-5" />

            <p class="w-75 mb-95">
              Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean. Separated they live in Bookmarksgrove.
            </p>

            <Button
              class="dark mb-95"
              content="Read More"
            />

            <div class="d-flex justify-content-between align-items-end ">

              <h6 class="text-uppercase fw-bold">facebook - instagram - youtube - twitter</h6>

              <div class="slide-counter d-flex justify-content-around align-items-center rounded-5">
                <div class="slide-number rounded-5">01</div>
                <div class="slide-number rounded-5 active">02</div>
                <div class="slide-number rounded-5">03</div>
              </div>

            </div>

          </div>

        </div>

      </div>

  </section>

</template>



<style lang="scss" scoped>

@use '../../assets/scss/partials/vars' as *;

  #jumbotron{
    padding: 160px 0 80px;
    background-color: $lg-1;
    background-image: url('../../assets/img/Group-35-2x.png');
    background-repeat: no-repeat;
    background-position: 175%;
    h6{
      
      letter-spacing: 1px;
      &.years17{
        @include gradient(bottom, $bg-green, #96e060);
        padding-left: 5px;
        letter-spacing: 10px;
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent; 
        -moz-background-clip: text;
        -moz-text-fill-color: transparent;
      }
    }
    .slide-counter{
      @include gradient(left, $gray-4, $gray-6);
      width: 200px;
      height: 50px;
      font-weight: bold;
      font-size: 1.3rem;
      color: $gray-5;
      .slide-number{
        width: 60px;
        height: 40px;
        text-align: center;
        line-height: 40px;
        &.active{
          @include gradient(bottom right, $bg-green, #96e060);
          color: #a6edb8;
        }
      }
    }
  }

</style>
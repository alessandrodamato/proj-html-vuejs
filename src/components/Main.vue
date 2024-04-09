<script>
import Jumbotron from './partials/Jumbotron.vue'
import DobuleLine from './partials/DobuleLine.vue';
import WhiteCard from './partials/WhiteCard.vue';
import Button from './partials/Button.vue'
  export default {
    components:{
      Jumbotron,
      DobuleLine,
      Button,
      WhiteCard
    }
  }
</script>



<template>

  <main>

    <Jumbotron />

    <section id="elegant">

      <div class="ad_container container-fluid">
        
        <div class="row">

          <div class="col-4">

            <h2 class="text-capitalize mb-4 mt-5">we are here to make your <span>website</span> look more <span>elegant</span> and stylish!</h2>

            <DobuleLine class="mb-5" />

            <Button content="view all" />

          </div>

          <div class="col-8 d-flex flex-wrap justify-content-end">

            <WhiteCard
              iconClass="fa-solid fa-gauge-high"
              title="Speed Optimization"
              bio="Far far away, behind the word mountains, far from the countries Vokalia Separated..."
            />
            <WhiteCard
              iconClass="fa-solid fa-cloud"
              title="Cloud Solutions"
              bio="Far far away, behind the word mountains, far from the countries Vokalia Separated..."
            />
            <WhiteCard
              iconClass="fa-solid fa-mobile-screen-button"
              title="Website Design"
              bio="Far far away, behind the word mountains, far from the countries Vokalia Separated..."
            />
            <WhiteCard
              iconClass="fa-solid fa-stopwatch"
              title="Online Marketing"
              bio="Far far away, behind the word mountains, far from the countries Vokalia Separated..."
            />

          </div>

        </div>

      </div>

    </section>

    <section id="missions" class="position-relative">

      <div class="ad_container container-fluid">
        
        <div class="row">

          <div class="col-8">

            <div class="architect-wrapper">
              <div class="architect position-relative overflow-hidden rounded-end-5">
                <img src="../assets/img/busy-architect-PYVKWM4-1024x872.jpg" alt="Busy Architect" class="img-fluid">
                <div class="architect-layer position-absolute top-0 start-0 w-100 h-100"></div>
              </div>
            </div>

            <div class="woman-wrapper position-absolute z-1 overflow-hidden rounded-5">
              <img src="../assets/img/businesswoman-analysing-document-P8WSNMC-1024x820.jpg" alt="Business Woman" class="img-fluid">
            </div>


          </div>

          <div class="col-4">

            <h2 class="mb-2 mt-5">learn more about our <span>missions</span></h2>

            <DobuleLine class="mb-3" />

            <p class="mb-5">
              Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean. Separated they live in Bookmarksgrove.
            </p>

            <Button content="read more" />

          </div>


        </div>

      </div>

    </section>

  </main>
  
</template>



<style lang="scss" scoped>

@use '../assets/scss/partials/vars' as *;

  #elegant{
    padding: 230px 0;
  }

  #missions{
    background-color: $lg-1;
    padding: 315px 0 290px;
    h2{
      padding-right: 100px;
    }
    img{
      width: 790px;
    }
    .architect-wrapper{
      position: absolute;
      top: 210px;
      left: 0;
     
      .architect-layer{
        @include gradient(bottom, rgba($bg-green, .7), rgba(#96e060, .7));
      }
    }
    .woman-wrapper{
        top: 310px;
        left: 130px;
      }
  }

</style>
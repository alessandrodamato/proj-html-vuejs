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

            <h2 class="text-capitalize mb-4 mt-5 pe-5">we are here to make your <span>website</span> look more <span>elegant</span> and stylish!</h2>

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

    <section id="missions">

      <div class="ad_container container-fluid">
        
        <div class="row">

          <div class="col-8 d-flex flex-wrap justify-content-end">

            <!-- //////////////////////////////////// images -->

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
    padding: 315px 0 290px;
    h2{
      padding-right: 100px;
    }
  }

</style>
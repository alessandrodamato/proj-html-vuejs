<script>
import { main } from '../data/db';
import Jumbotron from './partials/Jumbotron.vue'
import DoubleLine from './partials/DoubleLine.vue';
import Button from './partials/Button.vue';
import WhiteCard from './partials/WhiteCard.vue';
import ProjectCard from './partials/ProjectCard.vue';
  export default {
    components:{
      Jumbotron,
      DoubleLine,
      Button,
      WhiteCard,
      ProjectCard
    },

    data(){
      return{
        main
      }
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

            <DoubleLine class="mb-5" />

            <Button content="view all" />

          </div>

          <div class="col-8 d-flex flex-wrap justify-content-end position-relative">

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

            <div class="vertical">17 years of experience helping people for best solutions</div>

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

            <DoubleLine class="mb-3" />

            <p class="mb-5">
              Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean. Separated they live in Bookmarksgrove.
            </p>

            <Button content="read more" />

          </div>


        </div>

      </div>

    </section>

    <section id="projects">

      <div class="ad_container container-fluid">
        
        <div class="row">

          <div class="col-6">

            <DoubleLine class="mb-4" />

            <h2 class="mb-4">Our recent <span>web designs</span>  & some examples of past <span>projects</span></h2>

            <DoubleLine />

          </div>

          <div class="col-6 d-flex align-items-end">

            <p>
              Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean. Separated they live in Bookmarksgrove. Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove.
            </p>

          </div>

          <div class="col-12 position-relative">

            <div class="card-wrapper mt-80 mb-130 d-flex flex-wrap justify-content-between">

              <ProjectCard
                v-for="(card, index) in main.projectImages" :key="index"
                :name="card.name"
                :category="card.category"
                :path="card.path"
              />

              <div class="vertical">17 years of experience helping people for best solutions</div>

            </div>

          </div>

          <div class="col-12 text-center">

            <Button content="Read More" />

          </div>

        </div>

      </div>

    </section>

    <section id="plans">

      <div class="ad_container container-fluid">

        <div class="row">

          <div class="col-12">

            <div class="position-relative">

              <div class="stats position-relative overflow-hidden rounded-3">

                <img src="../assets/img/person-with-long-curly-hair-PZ99QM2-2x.jpg" alt="Stats" class="img-fluid w-100 h-100">

                <div class="stats-layer position-absolute top-0 start-0 w-100 h-100 text-white d-flex flex-column justify-content-center align-items-center ">

                  <div>

                    <div class="number">280</div>
                    <h6 class="text-uppercase fs-4 mb-5 text-center">projects</h6>
                    
                  </div>

                  <div class="d-flex">

                    <div class="text-center px-5 border-end">
                      <h4 class="fs-1">+3,500</h4>
                      <h6 class="text-uppercase fs-4">users' comments</h6>
                    </div>

                    <div class="text-center px-5">
                      <h4 class="fs-1">100%</h4>
                      <h6 class="text-uppercase fs-4">happy clients</h6>
                    </div>

                  </div>

                </div>

              </div>

              <div class="love rounded-3 position-absolute">

                <h2 class="text-capitalize">we <span>love</span> what we do</h2>

                <DoubleLine class="mb-4" />

                <p class="mb-5">
                  Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean. Separated they live in Bookmarksgrove. Far far away, behind the word mountains, a large language ocean, far from the countries Vokalia and Consonantia.
                </p>

                <ul>
                  <li>Far far away, behind the word mountains</li>
                  <li>Large language ocean</li>
                  <li>Far from the countries Vokalia and Consonantia</li>
                </ul>

              </div>

            </div>

          </div>

          <div class="col-12"></div>

        </div>

      </div>

    </section>

  </main>
  
</template>



<style lang="scss" scoped>

@use '../assets/scss/partials/vars' as *;

  #elegant, #projects{
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

  #plans{
    background-color: $lg-1;
    padding: 210px 0 230px;
    .stats, .love{
      width: 880px;
      height: 730px;
    }
    .stats{
      img{
        object-fit: cover;
        object-position: right
      }
      .stats-layer{
        @include gradient(top, rgba($bg-green, .8), rgba(#96e060, .8));
        .number{
          font-size: 8rem;
        }
        h6{
          color: #dff7e3;
        }
      }
    }
    .love{
      background-color: $fill-white;
      box-shadow: 0 0 20px 5px $lg-3;
      padding: 160px 100px;
      top: 90px;
      left: 750px;
      h2{
        padding-right: 200px;
      }
      li::before{
        font-family: 'Font Awesome 5 Free';
        content: '\f00c';
        display: inline-block;
        padding-right: 5px;
        vertical-align: middle;
        font-weight: 900;
        color: $text-green;
      }
    }
  }

</style>
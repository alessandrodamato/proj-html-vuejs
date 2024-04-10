<script>
import { main } from '../data/db';
import { store } from '../data/store';
import Jumbotron from './partials/Jumbotron.vue'
import DoubleLine from './partials/DoubleLine.vue';
import Button from './partials/Button.vue';
import WhiteCard from './partials/WhiteCard.vue';
import ProjectCard from './partials/ProjectCard.vue';
import PlanCard from './partials/PlanCard.vue';
import BlogCard from './partials/BlogCard.vue';
  export default {
    components:{
      Jumbotron,
      DoubleLine,
      Button,
      WhiteCard,
      ProjectCard,
      PlanCard,
      BlogCard
    },

    data(){
      return{
        main,
        store
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

            <Button content="view all" link="#" />

          </div>

          <div class="col-8 d-flex flex-wrap justify-content-end position-relative">

            <!-- alcuni font awesome sono differenti perché sono disponibili solo con versione pro -->

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

            <div class="vertical right">17 years of experience helping people for best solutions</div>

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

            <Button content="read more" link="#" />

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

              <div class="vertical right">17 years of experience helping people for best solutions</div>

            </div>

          </div>

          <div class="col-12 text-center">

            <Button content="Read More" link="#" />

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

          <div class="col-12 d-flex">

            <div class="text d-flex flex-column justify-content-center">

              <h2 class="text-capitalize">with <span>live chat 24/7</span> support</h2>

              <DoubleLine class="mb-4" />

              <p class="mb-5">
                Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics.
              </p>

            </div>

           <PlanCard
              class="theme-dark"
              title="designing"
              subtitle="All designs"
              price="13"
              type="Design"
            />
            <PlanCard
              class="theme-green" 
              title="development"
              subtitle="WordPress projects"
              price="15"
              type="Project"
            />
            <PlanCard 
              class="theme-dark"
              title="seo"
              subtitle="Web products"
              price="10"
              type="Product"
            />

          </div>

        </div>

      </div>

    </section>

    <section id="quote">

      <div class="wrapper w-100 h-100 text-center">

        <h2><span>&#x275B;&#x275B;</span></h2>

        <p class="mb-90">When it comes to barbequing, there are two main schools of thought for the tachniques that you can use. Freshly scrambled eggs with applewood smoked bacon - are amazing!</p>

        <div class="image mb-4 m-auto overflow-hidden">
          <img src="../assets/img/businesswoman-analysing-document-P8WSNMC-1024x820.jpg" alt="Lissa Durbin" class="w-100 h-100 object-fit-cover img-fluid ">
        </div>

        <h4 class="text-uppercase text-green">lissa durbin</h4>

        <h6>Client</h6>

      </div>

    </section>

    <section id="blog">

      <div class="ad_container container-fluid ">

        <div class="row">

          <div class="col-12 text-center">
            <h2 class="text-capitalize mb-4">latest news & our <span>blog</span></h2>
            <DoubleLine class="mb-5" />
          </div>
          
          <div class="col-4 d-flex justify-content-center position-relative">

            <div class="vertical left">17 years of experience helping people for best solutions</div>

            <BlogCard
              path="serious-businesswoman-with-documents-talking-on-P9Q6LX6-1024.jpg"
              date="May 24, 2024"
              author="Alex"
              title="Marketing Ideas"
            />
          </div>

          <div class="col-4 d-flex justify-content-center">
            <BlogCard
              path="Businessman-at-the-desk-in-his-office-resting--1024x768.jpg"
              date="May 24, 2024"
              author="Alex"
              title="Rest During Working Hours"
            />
          </div>

          <div class="col-4 d-flex justify-content-center">
            <BlogCard
              path="simple-home-office-with-tree-PBXRXYB-large-1024x768.jpg"
              date="May 24, 2024"
              author="Alex"
              title="Develop Your Startup Idea"
            />
          </div>

          <div class="col-12 text-center">

            <Button class="big dark" content="view all post" link="#" />
            
          </div>

          <div class="col-6 d-flex justify-content-end position-relative">

            <div class="padding"></div>

            <div class="big-card theme-dark rounded-4">

              <div class="question">Are You Ready?</div>

              <h3>Start a New Project</h3>

              <div class="input-bar rounded-5 mx-auto d-flex justify-content-between align-items-center overflow-hidden">
                <input class="w-100 h-100 px-5 bg-transparent border-0" type="email" placeholder="Enter Your Email Address" v-model="store.emailToSend" @keyup.enter="store.emailToSend = ''">
                <button class="h-100 pe-5 text-uppercase bg-transparent border-0" @click="store.emailToSend = ''" >Submit</button>
              </div>

            </div>
            
          </div>

          <div class="col-6 d-flex justify-content-start position-relative">

            <div class="padding"></div>

            <div class="big-card theme-green rounded-4">

              <div class="question">What Are You Waiting for?</div>

              <h3>Let's Talk About Work</h3>

              <Button class="dark shadow-none" content="start now" link="#" />
              
            </div>
            
          </div>
          
        </div>

      </div>

    </section>

    <section id="sponsors">

      <div class="ad_container container-fluid">

        <div class="row">

          <div class="col">
            
            <div class="content d-flex justify-content-around align-items-center w-100">

              <img v-for="(sponsor, index) in main.sponsors" :key="index" :src="`/img/${sponsor}`" alt="Sponsor">

            </div>

          </div>

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
        @include gradient(bottom left, rgba($bg-green, .8), rgba(#96e060, .8));
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
      margin-bottom: 530px;
      img{
        object-fit: cover;
        object-position: right
      }
      .stats-layer{
        @include gradient(top right, rgba($bg-green, .8), rgba(#96e060, .8));
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
      box-shadow: 10px 0 20px 5px $lg-3;
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

  #quote{
    height: 825px;
    background-image: url('../assets/img/four-businesspeople-in-a-boardroom-with-paperwork-PC4V8H4.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    .wrapper{
      @include gradient (right, rgba($bg-black, .9), rgba($gray-4, .9));
      padding: 180px 0 150px;
      p{
        padding: 0 480px;
        line-height: 40px;
        font-style: italic;
        font-size: 1.5rem;
        color: $lg-2;
      }
      h2{
        font-size: 7rem !important;
      }
      h6{
        color: $lg-2;
        font-size: 1.1rem;
      }
    }
    .image{
      width: 100px;
      aspect-ratio: 1 / 1;
      border: 4px solid $fill-white;
      border-radius: 50%;
    }
  }

  #blog{
    padding: 250px 0 0;
    .padding{
      min-height: 460px;
    }
    .big-card{
      width: 780px;
      height: 340px;
      padding: 70px 0;
      text-align: center;
      position: absolute;
      top: 100%;
      transform: translateY(-50%);
      .question{
        font-size: 1.1rem;
        font-weight: bold;
        margin-bottom: 10px;
      }
      h3{
        font-size: 2.5rem;
        font-weight: bold;
        color: $fill-white;
        margin-bottom: 70px
      }
      .input-bar{
        width: 480px;
        height: 65px;
        background-color: rgba($gray-6, .7);
        input{
          color: $lg-4;
          &:focus{
            outline: none;
          }
          &::placeholder{
            color: $lg-4;
          }
        }
        button{
          width: 100px;
          font-weight: bold;
          color: $lg-4;
          &:hover{
            opacity: .7;
          }
        }
      }
      &.theme-green{
        @include gradient(right, $bg-green, #96e060);
        .question{
          color: #c9f5d5;
        }
      }
      &.theme-dark{
        @include gradient(top left, $fill-black, $gray-6);
        color: $lg-5;
      }
    }
  }

  #sponsors{
    padding: 270px 0 125px;
    background-color: $lg-1;
  }

</style>
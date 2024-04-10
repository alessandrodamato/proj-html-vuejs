<script>
import { footer } from '../data/db';
import DoubleLine from './partials/DoubleLine.vue';
  export default {
    components:{
      DoubleLine
    },

    data(){
      return{
        footer
      }
    }
  }
</script>



<template>

  <footer>

    <div class="footer-top">

      <div class="ad_container container-fluid h-100">
        
        <div class="row row-cols-4 h-100">

          <div class="col h-100">

            <div class="logo mb-3">
              <a :href="footer.logo.href">
                <img :src="`/img/${footer.logo.image}`" :alt="footer.logo.name" class="img-fluid">
              </a>
            </div>

            <p>{{ footer.logo.bio }}</p>
            
          </div>

          <div class="col h-100">

            <h4 class="mt-1 mb-3">QUICk LINKS</h4>

            <DoubleLine class="mb-4" />

            <ul class="text-center">
              <li v-for="(link, index) in footer.links" :key="index" class="mt-1">
                <a :href="link.href">{{ link.name }}</a>
              </li>
            </ul>

          </div>

          <div class="col h-100">

            <h4 class="mt-1 mb-3">CONTACT</h4>

            <DoubleLine class="mb-4" />

            <p class="pe-5">{{ footer.contact.address }}</p>
            <p>{{ footer.contact.email }}</p>
            <p>{{ footer.contact.number }}</p>

          </div>

          <div class="col h-100">

            <h4 class="mt-1 mb-3">LOCATION ON MAP</h4>

            <DoubleLine class="mb-4" />

            <img src="/img/map.png" alt="Map" class="img-fluid">

          </div>

        </div>

      </div>

    </div>

    <div class="footer-bottom position-relative">

      <div class="ad_container container-fluid h-100">
        
        <div class="row h-100">

          <div class="col h-100 d-flex align-items-center">

           <p class="text-uppercase m-0 fs_08"><i class="fa-regular fa-copyright"></i> 2024 philox business theme.</p>

          </div>

          <div class="col-auto h-100 d-flex align-items-center">

            <div class="socials">
              <span v-for="(social, index) in footer.socials" :key="index" class="ms-3">
                <a :href="social.href" v-html="social.icon"></a>
              </span>
            </div>

          </div>

        </div>

      </div>

      <div class="buttons-wrapper position-absolute d-flex align-items-center">

        <button class="btn arrow d-flex justify-content-center align-items-center">
          <a :href="footer.buttons.arrow.href" v-html="footer.buttons.arrow.icon"></a>
        </button>

        <button class="btn message ms-3" v-html="footer.buttons.message.icon"></button>

      </div>

    </div>
    
  </footer>
  
</template>



<style lang="scss" scoped>

@use '../assets/scss/partials/vars' as *;

  footer{

    .footer-top{
      padding: 150px 0;
      p, a{
        color: $lg-7;
      }
      h4{
        font-weight: bold;
      }
    }

    .footer-bottom{
      height: 110px;
      @include gradient(left, $bg-black, $lg-7);
      p, a{
        color: $lg-4;
      }
      .buttons-wrapper{
        top: 15px;
        right: 40px;
        .arrow{
          width: 30px;
          height: 30px;
          font-size: .7rem;
          border-radius: 50%;
          background-color: $fill-white;
          a{
            color: $fill-black;
          }
        }
        .message{
          width: 60px;
          aspect-ratio: 1 / 1;
          transform: scaleX(-1);
          font-size: 1.7rem;
          border-radius: 50%;
          color: $fill-white;
          background-color: $bg-blue;
        }
      }
    }

  }

</style>
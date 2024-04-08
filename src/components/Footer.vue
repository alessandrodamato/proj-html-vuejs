<script>
import { footer } from '../data/db';
  export default {
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

            <p class="pe-3">{{ footer.logo.bio }}</p>
            
          </div>

          <div class="col h-100">

            <h4 class="mt-1 mb-3">QUICk LINKS</h4>

            <div class="ad_border sm mb-4"></div>
            <div class="ad_border xl mb-4"></div>

            <ul class="text-center">
              <li v-for="(link, index) in footer.links" :key="index" class="mt-1">
                <a :href="link.href">{{ link.name }}</a>
              </li>
            </ul>

          </div>

          <div class="col h-100">

            <h4 class="mt-1 mb-3">CONTACT</h4>

            <div class="ad_border sm mb-4"></div>
            <div class="ad_border xl mb-4"></div>

            <p class="pe-5">{{ footer.contact.address }}</p>
            <p>{{ footer.contact.email }}</p>
            <p>{{ footer.contact.number }}</p>

          </div>

          <div class="col h-100">

            <h4 class="mt-1 mb-3">LOCATION ON MAP</h4>

            <div class="ad_border sm mb-4"></div>
            <div class="ad_border xl mb-4"></div>

            <img src="/public/img/map.png" alt="Map" class="img-fluid">

          </div>

        </div>

      </div>

    </div>

    <div class="footer-bottom"></div>
    
  </footer>
  
</template>



<style lang="scss" scoped>

@use '../assets/scss/partials/vars' as *;

  footer{

    .footer-top{
      padding: 150px 0;
      p, a{
        color: $lg-5;
      }
      .ad_border{
        display: inline-block;
        border-radius: 3px;
        border: 3px solid $text-green;
        &.sm{
          width: 10px;
        }
        &.xl{
          margin-left: 5px;
          width: 50px;
        }
      }
    }

    .footer-bottom{
      height: 110px;
      background: $gradient-gray;
    }

  }

</style>
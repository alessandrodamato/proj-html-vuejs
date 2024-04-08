<script>
import { header } from '../data/db';
  export default {
    data(){
      return{
        header
      }
    }
  }
</script>



<template>

  <header>

    <div class="header-top text-white">

      <div class="ad_container-sm container-fluid h-100">
        
        <div class="row h-100">

          <div class="col h-100 d-flex align-items-center">

            <div class="numbers">
              <span class="me-2"><i class="fa-solid fa-phone"></i></span>
              <span v-for="(number, index) in header.numbers" :key="index" class="me-2">{{ number }}</span>
            </div>

          </div>
          <div class="col-auto h-100 d-flex align-items-center">

            <div class="socials">
              <span v-for="(social, index) in header.socials" :key="index" class="ms-3">
                <a :href="social.href" v-html="social.icon" class="text-white"></a>
              </span>
            </div>

          </div>

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
      background: linear-gradient(to left, $gray-3, #3b3b3b);
    }

    .header-bottom{
      height: 105px;
    }

  }

</style>
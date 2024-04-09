<script>
import { header } from '../data/db';
import Button from './partials/Button.vue'
  export default {
    components:{
      Button
    },

    data(){
      return{
        header
      }
    }
  }
</script>



<template>

  <header class="fs_09">

    <div class="header-top text-white">

      <div class="ad_container container-fluid h-100">
        
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

      <div class="ad_container container-fluid h-100">
        
        <div class="row row-cols-3 h-100">

          <div class="col h-100 d-flex justify-content-start align-items-center">

            <div class="logo">
              <a :href="header.logo.href">
                <img :src="`/img/${header.logo.image}`" :alt="header.logo.name" class="img-fluid">
              </a>
            </div>

          </div>

          <div class="col h-100 d-flex justify-content-center align-items-center">

            <nav class="h-100 d-flex align-items-center">

              <ul class="d-flex">

                <li v-for="(el, index) in header.menu" :key="index" class="mx-3">
                  <a
                    :href="el.href"
                    class="text-uppercase"
                    :class="{'active' : index === 0}"
                  >
                    {{ el.name }}
                  </a>
                </li>

              </ul>

            </nav>

          </div>

          <div class="col h-100 d-flex justify-content-end align-items-center">

            <div class="buttons-wrapper d-flex">

              <Button
                :link="header.buttons.purchase.href"
                :content="header.buttons.purchase.content"
              />

              <button
                class="search-button btn text-uppercase text-green ms-4 p-2 pe-0"
                v-html="header.buttons.search.icon"
              />
              
            </div>

          </div>

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
      @include gradient(left, $gray-3, #3b3b3b);
    }

    .header-bottom{
      height: 105px;
      .logo{
        width: 200px;
      }
      nav ul li a{
        color: $lg-6;
        &.active{
          color: $text-black-2;
        }
      }
      .search-button{
        border: none;
      }
    }
  }

</style>
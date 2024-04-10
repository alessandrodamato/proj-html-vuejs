<script>
  export default {
    props:{
      path: String,
      date: String,
      author: String,
      title: String,
    }
  }
</script>



<template>

  <div class="box position-relative border-0 rounded-3 mb-125">
    <img :src="`/src/assets/img/${path}`" :alt="title" class="w-100 h-100 object-fit-cover rounded-3">
    <div class="bio position-absolute z-1 rounded-3 d-flex flex-column justify-content-end">
      <span class="fs_09">{{ date }} &#x2022; by {{ author }}</span>
      <div class="position-relative">
        <div class="dot position-absolute"></div>
        <h4 class="m-0 mt-1 fw-bold">{{ title }}</h4>
      </div>
    </div>
  </div>

</template>



<style lang="scss" scoped>

@use '../../assets/scss/partials/vars' as *;

  .box{
    width: 510px;
    height: 390px;
    box-shadow: 0 0 20px 5px $lg-3;
    .bio{
      width: 430px;
      height: 125px;
      top: 100%;
      left: 50%;
      padding: 25px 40px;
      transform: translate(-50%, -50%);
      box-shadow: 0 10px 15px 1px $lg-3;
      background-color: $fill-white;
      .dot{
        width: 10px;
        height: 10px;
        margin-right: 2px;
        top: 50%;
        right: 100%;
        transform: translate(-50%, -25%);
        border-radius: 50%;
        background-color: $bg-green;
      }
      span{
        color: $lg-4;
      }
    }
  }

</style>
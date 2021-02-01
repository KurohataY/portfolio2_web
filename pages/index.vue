<template>
<v-app>
  <section v-if="loading" class="container">
    <div>
      <lottie :options="defaultOptions" v-on:animCreated="handleAnimation" />
    </div>
  </section>
  <section v-else>
    <div class="bg">
      <p>Portfolio</p>
    </div>
    <MainMenu />
  </section>
</v-app>
</template>

<script>
import Lottie from "~/components/Lottie.vue";
import * as animationData from "~/assets/animation/loadingAnimation.json";

import MainMenu from "~/components/mainMenu"

export default {
  components: {
    MainMenu,
    Lottie,
  },
  data() {
    return {
      // データを定義
      defaultOptions: {
        animationData: animationData
      },
      animationSpeed: 1,
      loading: true,
    };
  },
  created: function(){
    setTimeout(() => {
      this.loading = false}
      ,7000
    )
  },
  methods: {
    handleAnimation: function(anim) {
      this.anim = anim;
    }
  }
};
</script>

<style lang="scss" scoped>
.bg {
    background-image: url("~@/static/images/bg_pic-m.webp");
    width: 100%;
    height: 500px;
    object-fit: cover;
    // -ms-filter: blur(2px);
    // filter: blur(2px);
    position: relative;
    /*相対配置*/
    margin-bottom: 20px;
    p {
        position: absolute;
        /*絶対配置*/
        color: white;
        /*文字は白に*/
        top: 50%;
        left: 50%;
        -ms-transform: translate(-50%,-50%);
        -webkit-transform: translate(-50%,-50%);
        transform: translate(-50%,-50%);
        margin: 0;
        padding: 0;
        font-size: 70px;
    }
}
</style>

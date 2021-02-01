<template>
<section v-if="loading" class="container">
  <div>
    <lottie :options="defaultOptions" v-on:animCreated="handleAnimation" />
  </div>
</section>
</template>

<script>
import Lottie from "~/components/Lottie.vue";

// JSONデータを読み込み
import * as animationData from "~/assets/animation/loadingAnimation.json";

export default {
  components: {
    Lottie
  },
  data() {
    return {
      // データを定義
      defaultOptions: {
        animationData: animationData
      },
      animationSpeed: 1,
      loading: false,
    };
  },
  mounted() {
    this.anim = lottie.loadAnimation({
      container: this.$refs.lavContainer,
      renderer: "svg",
      loop: this.options.loop !== false,
      autoplay: this.options.autoplay !== false,
      animationData: this.options.animationData,
      rendererSettings: this.options.rendererSettings
    });
  },
  methods: {
    handleAnimation: function(anim) {
      this.anim = anim;
    },
    start() {
      this.anim.play();
      this.loading = true;
    },
    finish() {
      this.anim.stop();
      this.loading = false;
    },
  }
};
</script>

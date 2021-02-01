<template>
<v-container class="text-center">
  <h1>過去の制作物</h1>
  <v-row no-gutter>
    <v-col v-for="content of contents" cols="12" sm="6">
      <!-- ニュースカード（参考：https://qiita.com/KIYS/items/9805118aa86f35c7a852#%E5%AE%9F%E8%A3%85-6） -->
      <a :href="content.url" class="nuxtLink" :target="content.target">
        <v-card class="mx-auto" max-width="344">
          <v-img :src="content.image" height="200px"></v-img>
          <v-card-title>{{ content.title }}</v-card-title>
          <v-card-subtitle>{{ content.subtitle }}</v-card-subtitle>
        </v-card>
      </a>
    </v-col>
  </v-row>
</v-container>
</template>

<script>
export default {
  data: () => ({
    show: false,
    contents: [{
      image: "images/japaneseMidleName.webp",
      title: "Japanese Middle Name",
      subtitle: "日本古来の名前制度を試すことができます！初めての制作物なので、たまにデザイン直したりしてます。しかし、戒めのために残してます。",
      url: "https://middle-name.herokuapp.com/",
      target: "_blank",
    }, {
      image: "images/kanko.webp",
      title: "地方観光サイト",
      subtitle: "個人で開発した、勝手に地元を紹介するサイト（開発中）",
      url: "https://kesennuma-oshima-sightseeing.herokuapp.com/",
      target: "_blank",
    }, {
      image: "images/home.webp",
      title: "ポートフォリオサイト",
      subtitle: "ポートフォリオサイトとなっております。",
      url: "/",
      target: "",
    }, {
      image: "images/iOSApp.webp",
      title: "審判代行システム（iOS）",
      subtitle: "チーム開発した、審判を代行してくれるアプリのiOSアプリを開発しました。",
      url: "/iosdemo",
      target: "",
    }, ],
  })
}
</script>

<style lang="scss" scoped>
.nuxtLink {
    text-decoration: none;
}
</style>

<template>
<v-container class="text-center">
  <h1>プロフィール</h1>
  <div id="profile">
    <div class="" v-for="text of profile.text">
      <p>{{text}}</p>
    </div>
    <v-container>
      <v-row no-gutter>
        <v-col v-for="site of sites" cols="12" sm="6">
          <!-- ニュースカード（参考：https://qiita.com/KIYS/items/9805118aa86f35c7a852#%E5%AE%9F%E8%A3%85-6） -->
          <a class="nuxtLink" :href="site.url" target="_blank">
            <v-card class="mx-auto" max-width="344">
              <v-img :src="site.image" height="200px"></v-img>
              <v-card-title>{{ site.title }}</v-card-title>
            </v-card>
          </a>
        </v-col>
      </v-row>
    </v-container>
  </div>
</v-container>
</template>

<script>
export default {
  data: () => ({
    profile: {
      text: {
        n1: `みなさんこんにちは！地方で大学生をしています。イザナギと申します。`,
        n2: `このサイトは、ポートフォリオサイトです。簡単に自己紹介するために作成しました。`,
        n3: `私の趣味は漫画・アニメ・動画鑑賞やバイクでのツーリングや温泉など様々ありますが、`,
        n4: `温泉が一番好きですね！温泉に入ると肩こりが治りやすく、心が落ち着きますwww`,
        n5: `現在は様々なWebサイトを作成したりしております。`,
        n6: `開発したものはGitHubに、開発中の記録はブログに上げています。`,
      },
    },
    sites: [{
      url: "https://github.com",
      image: "images/Octocat.webp",
      title: "GitHub",
    }, {
      url: "https://izanagiblog.com",
      image: "images/blogImg.webp",
      title: "開発ブログ",
    }, ]
  })
}
</script>

<style lang="scss" scoped>
#profile {
    white-space: pre-line;
    font-size: 20px;
    margin: 50px 20px;
}
.nuxtLink {
    text-decoration: none;
}
</style>

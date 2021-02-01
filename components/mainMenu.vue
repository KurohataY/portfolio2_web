<template>
<v-container>
  <v-row no-gutter>
    <v-col v-for="content of contents" cols="12" sm="6">
      <!-- ニュースカード（参考：https://qiita.com/KIYS/items/9805118aa86f35c7a852#%E5%AE%9F%E8%A3%85-6） -->
      <nuxt-link :to="content.url" class="nuxtLink">
        <v-card class="mx-auto" max-width="344">
          <v-img :src="content.image" height="200px"></v-img>
          <v-card-title>{{ content.title }}</v-card-title>
          <v-card-subtitle>{{ content.subtitle }}</v-card-subtitle>
        </v-card>
      </nuxt-link>
    </v-col>
  </v-row>
</v-container>
</template>

<script>
export default {
  data: () => ({
    contents: [{
      image: "images/skill.webp",
      title: "スキル",
      subtitle: "現在取得しているスキル一覧です",
      url: "skill",
    }, {
      image: "images/profile.webp",
      title: "プロフィール",
      subtitle: "プロフィールをご紹介！",
      url: "profile",
    }, {
      image: "images/work.webp",
      title: "制作物",
      subtitle: "これまでに製作したものを載せております！",
      url: "work",
    }, {
      image: "images/contact.webp",
      title: "コンタクト",
      subtitle: "連絡先です",
      url: "contact",
    }, ],
  }),
}
</script>

<style lang="scss" scoped>
.nuxtLink {
    text-decoration: none;
}
</style>

<template>
<v-container class="text-center">
  <h1>スキル一覧</h1>
  <v-row no-gutter>
    <v-col v-for="skill of skills" cols="12" sm="4">
      <!-- ニュースカード（参考：https://qiita.com/KIYS/items/9805118aa86f35c7a852#%E5%AE%9F%E8%A3%85-6） -->
      <v-card class="mx-auto" max-width="344">
        <v-img :src="skill.image" height="200px"></v-img>
        <v-card-title>{{ skill.language }}</v-card-title>
        <v-card-subtitle>
          <div>フレームワーク</div>
          <span v-for="framework of skill.frameworks">
            {{ framework }}
          </span>
        </v-card-subtitle>
        <v-card-text>
          {{skill.text}}
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
  <h1>勉強中</h1>
  <v-row no-gutter>
    <v-col v-for="std_skill of std_skills" cols="12" sm="4">
      <!-- ニュースカード（参考：https://qiita.com/KIYS/items/9805118aa86f35c7a852#%E5%AE%9F%E8%A3%85-6） -->
      <v-card class="mx-auto" max-width="344">
        <v-img :src="std_skill.image" height="200px"></v-img>
        <v-card-title>{{ std_skill.language }}</v-card-title>
        <v-card-subtitle>
          <div>フレームワーク</div>
          <span v-for="framework of std_skill.frameworks">
            {{ framework }}
          </span>
        </v-card-subtitle>
      </v-card>
    </v-col>
  </v-row>
</v-container>
</template>

<script>
export default {
  data: () => ({
    show: true,
    skills: [{
      language: "JavaScript",
      frameworks: ["Nuxt.js", "Vue.js", "React.js", "Vuetify.js"],
      image: "images/javascript.webp",
      text: "",
    }, {
      language: "HTML",
      frameworks: ["　"],
      image: "images/html.webp",
      text: "",
    }, {
      language: "CSS",
      frameworks: ["　"],
      image: "images/css.webp",
      text: "",
    }, {
      language: "Ruby",
      frameworks: ["RubyonRails"],
      image: "images/ruby.webp",
      text: "",
    }, {
      language: "Python",
      frameworks: ["Flask"],
      image: "images/python.webp",
      text: "",
    }, ],
    std_skills: [{
      language: "Java",
      frameworks: ["Spring"],
      image: "images/java.webp",
      text: "",
    }, {
      language: "Swift",
      frameworks: ["UIkit", "SwiftUI"],
      image: "images/swift.webp",
      text: "",
    }, {
      language: "Golang",
      frameworks: ["Gin"],
      image: "images/go.webp",
      text: "",
    }, ],
  })
}
</script>

<style lang="scss" scoped>
</style>

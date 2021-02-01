<template>
  <v-container class="text-center">
    <h1>Contact</h1>
    <v-row no-gutter>
      <v-col v-for="contact of contacts" cols="12" sm="6">
        <a class="nuxtLink" :href="contact.url" target="_blank">
          <v-card class="mx-auto" max-width="344">
            <v-img :src="contact.image" height="200px"></v-img>
            <v-card-title>{{ contact.title }}</v-card-title>
          </v-card>
        </a>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    contacts: [{
      url: "https://twitter.com/COiod3nId8QqtKv",
      title: "Twitter",
      image: "/images/twitter.webp"
    },{
      url: "https://forms.gle/yRVxv1HK5vRRSmtx9",
      title: "Googleフォーム",
      image: "/images/googleform.webp"
    },]
  })
}
</script>

<style lang="scss" scoped>
  .nuxtLink {
    text-decoration: none;
  }
</style>

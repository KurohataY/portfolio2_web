<template>
<div class="text-right blue">
  <v-menu offset-y>
    <template v-slot:activator="{ on }">
      <v-btn color="blue" dark v-on="on">
        <i class="mdi mdi-menu" />
      </v-btn>
    </template>
    <v-list>
      <v-list-item v-for="(item, index) in items" :key="index" @click="">
        <v-list-item-title>
          <nuxt-link :to="item.url" class="nuxtLink orange--text">{{ item.title }}</nuxt-link>
        </v-list-item-title>
      </v-list-item>
    </v-list>
  </v-menu>
</div>
</template>

<script>
export default {
  data: () => ({
    items: [{
        title: 'ホーム',
        url: "/",
      },
      {
        title: 'スキル',
        url: "skill",
      },
      {
        title: 'プロフィール',
        url: "profile",
      },
      {
        title: '制作物',
        url: "work",
      },
      {
        title: 'コンタクト',
        url: "contact",
      },
    ],
  }),
}
</script>

<style lang="scss" scoped>
.nuxtLink {
    text-decoration: none;
}
</style>

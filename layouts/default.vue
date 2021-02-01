<template>
<v-app>
  <header>
    <Mmenu />
  </header>
  <main>
    <nuxt />
  </main>
  <v-footer>
    <Fmenu />
  </v-footer>
</v-app>
</template>

<script>
import Mmenu from "~/components/menu.vue"
import Fmenu from "~/components/footerMenu.vue"

export default {
  components: {
    Mmenu,
    Fmenu,
  }
}
</script>
<style lang="scss" scoped>

</style>

<template>
  <div class="container">
    <Header />
    <Nuxt />
  </div>
</template>

<script>
import Header from '~/components/Header/Main.vue'

export default {
  components: {
    Header,
  },
  data () {
    return {
    }
  }
}
</script>

<style lang="scss" scoped>
</style>

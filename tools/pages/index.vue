<template>
  <div class="container">
    <VideoSection />

    <div class="second-section">
      <h2>This section is only text</h2>
    </div>
  </div>
</template>

<script>
import VideoSection from '~/components/Container/TopPage/Video.vue'

export default {
  name: 'IndexPage',
  components: {
    VideoSection,
  },
  data () {
    return {
    }
  }
}
</script>

<style lang="scss" scoped>
.second-section {
  width: 100%;
  min-height: 100vh;
  background-color: #111;
  color: #fff;
}
</style>

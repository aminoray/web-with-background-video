<template>
  <div
    class="container"
    :class="{ cannotScroll : isLoading }"
    >
    <!-- <LoadingSimple
      :loading-flag="isLoading"
    /> -->
    <DistortedQuadrilateral
      :loading-flag="isLoading"
    />

    <VideoSection
      class="content"
      :class="{ loading : isLoading  }"
    />

    <div class="second-section">
      <h2>This section is only text</h2>
    </div>
  </div>
</template>

<script>
import VideoSection from '~/components/Container/TopPage/Video.vue'
import LoadingSimple from '~/components/Loading/Simple.vue'
import DistortedQuadrilateral from '~/components/Loading/DistortedQuadrilateral.vue'

export default {
  name: 'IndexPage',
  components: {
    VideoSection,
    LoadingSimple,
    DistortedQuadrilateral,
  },
  data () {
    return {
      isLoading: true,
    }
  },
  mounted() {
    setTimeout(() => {
      this.isLoading = false
    }, 1500)
  },
}
</script>

<style lang="scss" scoped>
.cannotScroll {
  height: 100vh;
  overflow-y: hidden;
}
.content {
  transition: all 0.4s;
  transition-delay: 0.1s;
}
.loading {
  visibility: hidden;
}
.second-section {
  width: 100%;
  min-height: 100vh;
  background-color: #fff;
  color: #8e8e8e;
}
</style>

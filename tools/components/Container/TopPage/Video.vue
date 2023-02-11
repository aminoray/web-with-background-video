<template>
  <div class="video-section">
    <video :src="videoPath" autoplay muted loop></video>
    <div class="overlay"></div>
  </div>
</template>

<script>
export default {
  name: 'VideoSection',
  data () {
    return {
      // ここに挿入したいビデオのパスを入れてね
      videoPath: require("~/assets/videos/myoko.mp4")
    }
  }
}
</script>

<style lang="scss" scoped>
.video-section {
  position: relative;
  width: 100%;
  min-height: 100vh;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #111;
  margin: 0;

  video {
    position: absolute;
    top: 0;
    left: 0%;
    width: 100%;
    height: 100%;
    object-fit: cover;
    opacity: 0.8;
  }

  .overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color:#999999;
    mix-blend-mode: overlay;
  }
}
</style>

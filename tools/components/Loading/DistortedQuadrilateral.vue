<template>
  <div class="container" :class="{ loaded : !loadingFlag }">
    <div class="loader">
      <span></span>
      <span></span>
      <span></span>
      <h2>Now Loading...</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DistortedQuadrilateral',
  components: {
  },
  props: {
    loadingFlag: {
      type: Boolean,
      default: true,
    },
  },
  data () {
    return {
    }
  }
}
</script>

<style lang="scss" scoped>
.container {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  min-height: 100vh;
  background-color: #fff;
  color: #8f8f8f;
  z-index: 9999;
  display: flex;
  justify-content: center;
  align-items: center;
}

.loaded {
  opacity: 0;
  visibility: hidden;
  transition: all 1s;
}

.loader {
  position: relative;
  width: 400px;
  height: 400px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.loader span {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 3px solid #80c5de;
  animation: animate 5s linear infinite;
}

.loader span:nth-child(1) {
  /* border-radius: 50%; */
  border-radius: 86% 14% 55% 45% / 25% 68% 32% 75%;
}

.loader span:nth-child(2) {
  animation-direction: reverse;
  border-radius: 32% 68% 11% 89% / 63% 32% 68% 37%;
}

.loader span:nth-child(3) {
  animation-duration: 3s;
  border-radius: 43% 57% 55% 45% / 82% 60% 40% 18%;
}

@keyframes animate {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>

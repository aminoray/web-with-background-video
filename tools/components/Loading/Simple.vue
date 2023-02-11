<template>
  <div class="container" :class="{ loaded : !loadingFlag }">
    <div class="icon">
      <img src="~/assets/gif/loading-gif.gif" alt="">
      <h2>Loading...</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LoadingSimple',
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
  color: #666666;
  z-index: 9999;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: all 0.4s;

  .icon {
    width: auto;
    height: auto;
    text-align: center;
    img {
      width: 64px;
      height: auto;
    }

    h2 {
      margin-top: 10px;
      font-size: 1rem;
      color: #ababab;
    }
  }
}

.loaded {
  opacity: 0;
  visibility: hidden;
  transition: all 1s;
}
</style>

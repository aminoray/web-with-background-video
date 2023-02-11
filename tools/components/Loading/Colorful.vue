<template>
  <div class="container" :class="{ loaded : !loadingFlag }">
    <div class="icon">
      <img src="~/assets/gif/colorful.gif" alt="Colorful">
      <h2>Now Loading...</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Colorful',
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
  background-color: #fcfcff;
  z-index: 9999;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: all 0.4s;

  .icon {
    width: 340px;
    height: auto;
    text-align: center;
    position: relative;
    img {
      width: 100%;
      height: auto;
    }

    h2 {
      width: 100%;
      position: absolute;
      bottom: 20px;
      font-size: 1rem;
      color: #8e8e8e;
    }
  }
}

.loaded {
  opacity: 0;
  visibility: hidden;
  transition: all 1s;
}
</style>

<template>
  <button
    class="button-body"
  >
    <font-awesome-icon icon="magnifying-glass" style="font-size: 16px" class="icon" />
    {{ text }}
  </button>
</template>

<script>
export default {
  name: 'RectangleWithIcon',
  props: {
    text: {
      type: String,
      default: ''
    },
    size: {
      type: String,
      default: 'M'
    }
  },
  data () {
    return {
    }
  }
}
</script>

<style lang="scss" scoped>
button {
  width: 200px;
  cursor: pointer;
  padding: 10px 20px;
  background-color: #8BC6EC;
  background-image: linear-gradient(135deg, #8BC6EC 0%, #9599E2 100%);
  color: #fff;
  text-align: center;
  position: relative;
}

button:hover {
  transition: all 0.4s;
  opacity: 0.5;
}

.icon {
  position: absolute;
  left: 15px;
}
</style>

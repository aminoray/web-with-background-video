<template>
  <button class="button-body" @click="$emit('onClickButton')">
    {{ text }}
  </button>
</template>

<script>
export default {
  name: 'RectangleRoundCorner',
  props: {
    text: {
      type: String,
      default: ''
    },
  },
  data () {
    return {
    }
  }
}
</script>

<style lang="scss" scoped>
button {
  width: 120px;
  border-radius: 6px;
  cursor: pointer;
  padding: 10px 20px;
  background-color: #8BC6EC;
  background-image: linear-gradient(135deg, #8BC6EC 0%, #9599E2 100%);
  color: #fff;
  text-align: center;
}

button:hover {
  transition: all 0.4s;
  opacity: 0.5;
}
</style>

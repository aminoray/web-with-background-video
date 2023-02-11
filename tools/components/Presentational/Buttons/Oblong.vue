<template>
  <button
    class="button-body"
  >
    {{ text }}
  </button>
</template>

<script>
export default {
  name: 'Oblong',
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
  width: 180px;
  cursor: pointer;
  padding: 15px 20px;
  border-radius: 60px;
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

<template>
  <Button class="button-body">
    {{ text }}
  </Button>
</template>

<script>
export default {
  name: 'Rectangle',
  props: {
    text: {
      type: String,
      default: ''
    }
  },
  data () {
    return {
    }
  }
}
</script>

<style lang="scss" scoped>
.button-body {
  width: 120px;
  cursor: pointer;
  padding: 10px 20px;
  background-color: cornflowerblue;
  color: #fff;
  text-align: center;
}
</style>

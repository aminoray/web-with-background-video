<template>
  <div class="container">
    <div class="title-section">
      <h2>
        このページではさまざまなボタンのサンプルを示すよ
      </h2>
    </div>

    <div class="buttons-section">
      <div class="card">
        <h3 class="name">一般的なボタン</h3>
        <Rectangle
          text="hoge"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Rectangle from '~/components/Presentational/Buttons/Rectangle.vue'

export default {
  name: 'Buttons',
  components: {
    Rectangle,
  },
  data () {
    return {
    }
  }
}
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  padding-top: 60px;

  .buttons-section {
    display: flex;
    flex-wrap: wrap;
  }
}

.card {
  background-color: #8d8d8d;
  border-radius: 10px;
  width: 320px;
  height: 180px;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;

  .name {
    position: absolute;
    top: 10px;
    left: 10px;
    font-size: 1rem;
    color: #E8E8E8E8;
  }
}
</style>

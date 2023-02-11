<template>
  <div class="container">
    <div class="title-section">
      <h2>
        Blog
      </h2>
      <p>This page features samples of various types of buttons.</p>
    </div>

    <div class="buttons-section">
      <div class="card">
        <h3 class="name">Rectangle</h3>
        <Rectangle
          text="hoge"
          size="M"
        />
      </div>

      <div class="card">
        <h3 class="name">RectangleRoundCorner</h3>
        <RectangleRoundCorner
          text="hoge"
          size="M"
        />
      </div>

      <div class="card">
        <h3 class="name">RectangleWithIcon </h3>
        <RectangleWithIcon
          text="search"
        />
      </div>

      <div class="card">
        <h3 class="name">Oblong</h3>
        <Oblong
          text="hoge"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ArticleIndex',
  components: {
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

  .title-section {
    margin: 20px;

    h2 {
      font-size: 2rem;
      color: #5e5e5e;
    }

    p {
      font-size: 1rem;
      color: #8e8e8e;
    }
  }
}

.card {
  background-color: #fff;
  box-shadow: 0 8px 10px 1px rgba(0, 0, 0, .2), 0 0 5px rgba(0, 0, 0, .1);
  border-radius: 10px;
  width: 300px;
  height: 180px;
  margin: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;

  .name {
    position: absolute;
    top: 10px;
    left: 10px;
    font-size: 1rem;
    font-weight: 200;
    color: #8e8e8e;
  }
}
</style>

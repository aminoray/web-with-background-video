<template>
  <div class="container">
    <LoadingSimple
      :loading-flag="selectedLoadingPage === 'LoadingSimple'"
    />
    <DistortedQuadrilateral
      :loading-flag="selectedLoadingPage === 'DistortedQuadrilateral'"
    />
    <Coolest
      :loading-flag="selectedLoadingPage === 'Coolest'"
    />

    <div class="title-section">
      <h2>
        Samples of Loading page
      </h2>
      <p>On this page, you can view samples of loading screens. Please press a button and try it out.</p>
    </div>

    <div class="samples-section">
      <div class="card">
        <img src="~/assets/images/loading/loading-1.jpg" alt="LoadingSimple">
        <h3 class="name">LoadingSimple</h3>
        <p class="description">This loading screen is the simplest one.</p>
        <RectangleRoundCorner
          text="open"
          size="M"
          @onClickButton="openLoadingPage('LoadingSimple')"
        />
      </div>

      <div class="card">
        <img src="~/assets/images/loading/loading-2.jpg" alt="LoadingSimple">
        <h3 class="name">DistortedQuadrilateral</h3>
        <p class="description">This loading screen indicates that it is currently loading with a distorted square rotating.</p>
        <RectangleRoundCorner
          text="open"
          size="M"
          @onClickButton="openLoadingPage('DistortedQuadrilateral')"
        />
      </div>

      <div class="card">
        <img src="~/assets/images/loading/loading-3.jpg" alt="LoadingSimple">
        <h3 class="name">Coolest</h3>
        <p class="description">This loading page is a loading screen characterized by circles and triangles</p>
        <RectangleRoundCorner
          text="open"
          size="M"
          @onClickButton="openLoadingPage('Coolest')"
        />
      </div>
    </div>

    <RectangleRoundCorner
      v-if="selectedLoadingPage.length > 0"
      class="close-button"
      text="close"
      size="M"
      @onClickButton="close()"
    />
  </div>
</template>

<script>
import LoadingSimple from '~/components/Loading/Simple.vue'
import DistortedQuadrilateral from '~/components/Loading/DistortedQuadrilateral.vue'
import RectangleRoundCorner from '~/components/Presentational/Buttons/RectangleRoundCorner.vue'
import Coolest from '~/components/Loading/Coolest.vue'

export default {
  name: 'LoadingPage',
  components: {
    LoadingSimple,
    DistortedQuadrilateral,
    RectangleRoundCorner,
    Coolest,
  },
  data () {
    return {
      selectedLoadingPage: ''
    }
  },
  mounted() {
  },
  methods: {
    openLoadingPage (page) {
      this.selectedLoadingPage = page
    },
    close () {
      this.selectedLoadingPage = ''
    }
  }
}
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  .title-section {
    margin: 80px 30px 30px;

    h2 {
      font-size: 2rem;
      color: #5e5e5e;
    }

    p {
      font-size: 1rem;
      color: #8e8e8e;
    }
  }

  .samples-section {
    display: flex;
    flex-wrap: wrap;
    margin: 20px;
  }
}

.card {
  background-color: #fff;
  box-shadow: 0 8px 10px 1px rgba(0, 0, 0, .2), 0 0 5px rgba(0, 0, 0, .1);
  border-radius: 10px;
  width: auto;
  height: auto;
  padding: 20px;
  margin: 15px;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  flex-direction: column;

  .name {
    width: 240px;
    text-align: left;
    font-size: 1rem;
    font-weight: 200;
    color: #8e8e8e;
    margin-top: 5px;
  }

  .description {
    width: 240px;
    min-height: 100px;
    text-align: left;
    font-size: 0.9rem;
    margin: 5px 0 10px;
  }

  img {
    width: 240px;
    height: 240px;
    border: 1px solid #8e8e8e;
  }
}

.cannotScroll {
  height: 100vh;
  overflow-y: hidden;
}
.content {
  transition: all 0.4s;
  transition-delay: 0.1s;
}

.close-button {
  position: fixed;
  z-index: 10000;
  top: 20px;
  right: 20px;
}
</style>

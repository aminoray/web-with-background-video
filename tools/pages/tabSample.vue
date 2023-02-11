<template>
  <div class="container">
    <div class="title-section">
      <h2>
        Samples of Tab switch
      </h2>
      <p>On this page, you can view samples of loading screens. Please press a button and try it out.</p>
    </div>

    <div class="tab-section">
      <ul>
        <li :class="{ selected : selectedTab === 1 }">
          <a @click="tabSwitch(1)">
            <font-awesome-icon icon="code" style="font-size: 16px" class="icon" />
            tab1
          </a>
        </li>

        <li :class="{ selected : selectedTab === 2 }">
          <a @click="tabSwitch(2)">
            <font-awesome-icon icon="user" style="font-size: 16px" class="icon" />
            tab2
          </a>
        </li>

        <li :class="{ selected : selectedTab === 3 }">
          <a @click="tabSwitch(3)">
            <font-awesome-icon icon="file" style="font-size: 16px" class="icon" />
            tab3
          </a>
        </li>

        <li :class="{ selected : selectedTab === 4 }">
          <a @click="tabSwitch(4)">
            <font-awesome-icon icon="image" style="font-size: 16px" class="icon" />
            tab4
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'tabSample',
  components: {
  },
  data () {
    return {
      selectedTab: 1,
    }
  },
  mounted() {
  },
  methods: {
    tabSwitch (tab) {
      this.selectedTab = tab
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
}

.tab-section {
  margin: 15px 30px;
  ul {
    border-bottom: 1px solid #8e8e8e;
    align-items: center;
    display: flex;
    li {
      display: inline-flex;
      border-bottom: 2px solid #fefefe;
      padding: 5px 10px;

      a {
        font-size: 1.2rem;
        line-height: 1.5rem;
        padding: 3px 10px;
        border-radius: 5px;
        cursor: pointer;
      }

      a:hover {
        transition: all 0.4s;
        background-color: #cfcfcf5b;
      }
    }

    .selected {
      border-bottom: 2px solid #ff984e;
    }
  }
}
</style>
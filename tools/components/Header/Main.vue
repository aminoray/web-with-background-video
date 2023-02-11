<template>
  <div class="container">
    <div class="logo-section">
      LOGO
    </div>
    <div class="navigation">
      <ul>
        <li>
          <NuxtLink to="/" class="link">HOME</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/buttons" class="link">BUTTONS</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/loading" class="link">LOADING</NuxtLink>
        </li>
      </ul>
    </div>
  </div>
</template>

<script></script>

<style lang="scss" scoped>
.container {
  position: fixed;
  width: 100%;
  height: 60px;
  background-color: #3556623a;
  z-index: 1000;
  display: flex;
  top: 0;
  justify-content: space-between;
  align-items: center;
}

.logo-section {
  margin-left: 20px;
  color: #fff;
}

.navigation {
  margin-right: 20px;

  ul {
    li {
      display: inline;
      text-decoration: none;
      margin-left: 10px;

      .link {
        font-size: 1rem;
        color: #fff;
        text-decoration: none;
        cursor: pointer;
      }

      .link:hover {
        transition: all 0.4s;
        color: aquamarine;
      }
    }
  }
}
</style>

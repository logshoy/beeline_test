<template>
  <div class="layout">
    <Headers />
    <main class="layout__main">
      <aside class="layout__aside"><SideBar /></aside>
      <div class="view"><router-view /></div>
    </main>
  </div>
</template>

<script>
// @ is an alias to /src
import Headers from "@/components/Header/Headers.vue";
import SideBar from "@/components/SideBar/SideBar.vue";

export default {
  components: {
    Headers,
    SideBar,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: linear-gradient(
    135deg,
    rgba(255, 255, 255, 0.0001) 0%,
    rgba(255, 255, 255, 0.1) 100%
  );
  mix-blend-mode: normal;
  width: 100%;
  height: 100vh;
  height: -webkit-fill-available;
  overflow-x: hidden;
  max-height: 100%;
}

ul {
  list-style: none;
}

.view {
  margin: 0;
  padding: 0;
  margin-left: 25%;
  margin-right: 10vh;
  margin-top: 10vh;
  width: 100%;
}

.layout {
  display: flex;
  position: relative;

  &__main {
    display: flex;
    // order: 2;
    margin-top: 10vh;
    flex: 1 0 auto;
  }
  &__aside {
    // order: 1;
    width: 20%;
    flex: 0 0 auto;
    height: 100vh;
    position: fixed;
    z-index: 30;
    @media (max-width: 767px) {
      display: none;
    }
  }
}
</style>

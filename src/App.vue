<template>
  <div class="layout">
    <aside class="layout__aside"><SideBar /></aside>
    <main class="layout__main">
      <Headers />
      <router-view />
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
  height: 100vh;
  height: -webkit-fill-available;
  max-height: 100vh;
  overflow-x: auto;
  overflow-y: hidden;
}

.layout {
  display: flex;
  height: 100vh;

  &__main {
    order: 2;
    width: auto;
    flex: 1 0 auto;
  }
  &__aside {
    order: 1;
    width: 300px;
    flex: 0 0 auto;
    height: 100vh;
  }
}
</style>

<template>
  <header
    class="d-flex flex-wrap justify-content-center py-3 mb-4 border-bottom sticky"
  >
    <LinkHeader />
    <ProfileBlock />
  </header>
</template>

<script>
// @ is an alias to /src
import LinkHeader from "@/components/Header/LinkHeader.vue";
import ProfileBlock from "@/components/Header/ProfileBlock.vue";

export default {
  name: "HomeView",
  components: {
    LinkHeader,
    ProfileBlock,
  },
};
</script>

<style>
.sticky {
  position: fixed;
  top: 0;
  z-index: 100;
  width: 100%;
  height: 10vh;
  background: green;
}
</style>

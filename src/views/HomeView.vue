<template>
  <div>
    <SliderBlock />
  </div>
</template>

<script>
// @ is an alias to /src
import SliderBlock from "@/components/Main/SliderBlock.vue";

export default {
  name: "HomeView",
  components: {
    SliderBlock,
  },
};
</script>

<style lang="scss">
.home {
  margin: auto 54px;
}
</style>

<template>
  <div class="home">
    <SliderBlock />
    <img alt="Vue logo" src="../assets/logo.png" />
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

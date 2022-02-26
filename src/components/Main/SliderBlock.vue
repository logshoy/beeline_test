<template>
  <div class="main__">
    <div>
      <HeaderSlider />
      <ListSlider />
    </div>
    <div>
      <HeaderSlider />
      <ListSlider />
    </div>
  </div>
</template>

<script>
import HeaderSlider from "@/components/Main/HeaderSlider.vue";
import ListSlider from "@/components/Main/ListSlider.vue";

export default {
  components: {
    HeaderSlider,
    ListSlider,
  },
};
</script>

<style></style>

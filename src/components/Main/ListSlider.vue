<template>
  <ul class="flex">
    <li class="sliderItem"><SliderItem /></li>
    <li class="sliderItem"><SliderItem /></li>
    <li class="sliderItem"><SliderItem /></li>
    <li class="sliderItem"><SliderItem /></li>
  </ul>
</template>

<script>
import SliderItem from "@/components/Main/SliderItem.vue";
export default {
  components: {
    SliderItem,
  },
};
</script>

<style>
.sliderItem {
  width: 40vh;
  margin: 5px;
}
</style>

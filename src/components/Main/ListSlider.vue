<template>
  <div class="album">
    <ul class="container flex">
      <li v-for="item in items" v-bind:key="item.id">
        <SliderItem />
      </li>
      <!-- <li class="sliderItem"><SliderItem /></li>
      <li class="sliderItem"><SliderItem /></li>
      <li class="sliderItem"><SliderItem /></li>
      <li class="sliderItem"><SliderItem /></li> -->
    </ul>
  </div>
</template>

<script>
import SliderItem from "@/components/Main/SliderItem.vue";
export default {
  data() {
    return {
      items: ["1", "2", "3", "4", "5"],
    };
  },
  components: {
    SliderItem,
  },
};
</script>

<style>
.sliderItem {
  width: 25%;
  max-width: 25%;
  margin: 5px;
}
</style>

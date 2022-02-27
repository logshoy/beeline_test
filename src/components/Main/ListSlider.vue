<template>
  <v-sheet class="mx-auto" elevation="8" max-width="800">
    <v-slide-group class="pa-4" center-active show-arrows>
      <v-slide-item flex v-for="n in 5" :key="n">
        <v-card class="ma-4" height="200" width="100">
          <v-row class="fill-height" justify="center"> </v-row>
        </v-card>
      </v-slide-item>
    </v-slide-group>
  </v-sheet>
</template>

<script>
export default {
  data: () => ({
    model: null,
    active: true,
    toggle: true,
  }),
};
</script>

<style></style>

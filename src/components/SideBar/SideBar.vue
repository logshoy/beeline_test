<template>
  <v-navigation-drawer permanent>
    <div class="flex">
      <v-img
        class="mx-2"
        src="https://i.imgur.com/qgGY4tB.png"
        max-height="40"
        max-width="40"
        contain
      ></v-img>
      <v-toolbar-title class="ml-2"> Page title </v-toolbar-title>
    </div>
    <v-list>
      <v-list-item v-for="item in items" :key="item.title" link>
        <v-list-item-icon>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>

    <template v-slot:append>
      <div class="pa-2">
        <v-btn block> Logout </v-btn>
      </div>
    </template>
  </v-navigation-drawer>
</template>

<script>
export default {};
</script>

<style></style>

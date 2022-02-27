<template>
  <v-app id="inspire">
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
    <v-app-bar app color="black">
      <!-- <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon> -->

      <!-- <v-toolbar-title>Application</v-toolbar-title> -->
      <v-list class="flex">
        <div class="button" v-for="item in link" :key="item.title">
          <v-button>{{ item.title }}</v-button>
        </div>
      </v-list>
    </v-app-bar>

    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
export default {
  components: {},
  data: () => ({
    drawer: !null,
    items: [
      { title: "Dashboard", icon: "mdi-view-dashboard" },
      { title: "Account", icon: "mdi-account-box" },
      { title: "Admin", icon: "mdi-gavel" },
    ],
    link: [{ title: "Faq" }, { title: "Faq" }, { title: "Faq" }],
  }),
};
</script>

<style scoped>
#app {
  height: 100%;
  margin: 0;
  padding: 0;
}

.height100 {
  margin-top: 64px;
  min-height: 100vh;
}

.button {
  margin: 5px;
  padding: 5px;
}

.mainS {
  margin-left: 20vh;
  margin-bottom: 64px;
}

.flex {
  display: flex;
}
</style>

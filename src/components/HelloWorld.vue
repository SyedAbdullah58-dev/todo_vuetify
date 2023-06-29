<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer" app
  >
    <v-list-item>
      <v-list-item-content prepend-icon="mdi-view-dashboard" class="title">Tech-Mentor</v-list-item-content>
    </v-list-item>
    <v-list-item-subtitle>
      Your future guide
    </v-list-item-subtitle>
<v-divider></v-divider>
<v-List
dense nav>
<vlist-item v-for="it in items" :key="it.title">
  <v-list-item-icon><v-icon>{{it.icon}}</v-icon></v-list-item-icon>
  <v-list-item-content><v-list-item-title>
    {{it.title}}</v-list-item-title>
  </v-list-item-content>
</vlist-item>
</v-List>
    <template v-slot:append>
      <div class="pa-2">
        <v-btn block>
          Logout
        </v-btn>
      </div>
    </template>
  </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Application</v-toolbar-title>
    </v-app-bar>
    <v-main></v-main>
  </v-app>
</template>

<script> /* eslint-disable */
export default {
  data: () => (
   {
      drawer: null,
      items: [
        { title: 'Dashboard',icon:'mdi-view-dashboard'},
        { title: 'My Account', icon: 'mdi-account' },
        { title: 'Users', icon: 'mdi-account-group-outline' }
      ],
      rail: false
    } )

}</script>

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
<v-list-item v-for="it in items" :key="it.title" :to="it.to" link>
  <v-list-item-icon><v-icon>{{it.icon}}</v-icon></v-list-item-icon>
  <v-list-item-content><v-list-item-title>
    {{it.title}}</v-list-item-title>
  </v-list-item-content>
</v-list-item>
</v-List>
    <template v-slot:append>
      <div class="pa-2">
        <v-btn block>
          Logout
        </v-btn>
      </div>
    </template>
  </v-navigation-drawer>

  <v-app-bar app
  color="primary"
  dark
  src="just.jpeg"
  prominent
>
  <template v-slot:image="{props}">
    <v-img
    v-bind="props"
      gradient="to top right, rgba(19,84,122,.8), rgba(128,208,199,.8)"
    ></v-img>
  </template>

    <v-app-bar-nav-icon @click="drawer=!drawer"></v-app-bar-nav-icon>
  <v-app-bar-title>Todo</v-app-bar-title>

  <v-spacer></v-spacer>

  <v-btn icon>
    <v-icon>mdi-magnify</v-icon>
  </v-btn>

  <v-btn icon>
    <v-icon>mdi-heart</v-icon>
  </v-btn>

  <v-btn icon>
    <v-icon>mdi-dots-vertical</v-icon>
  </v-btn>
</v-app-bar>
    <v-main><router-view></router-view></v-main>
  </v-app>
</template>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
<script> /* eslint-disable */
export default {
  data: () => (
   {
      drawer: null,
      items: [
        { title: 'todo',icon:'mdi-format-list-checks',to:'/home'},
        { title: 'About', icon: 'mdi-help-box',to:'/about' }

      ],
      rail: false
    } )

}</script>
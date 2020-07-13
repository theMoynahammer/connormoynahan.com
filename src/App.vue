<template>
  <v-app>
    <!-- <v-app-bar
      app
      color="#4682B4"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Headshot"
          class="shrink mr-2 headshot-navbar"
          contain
          :src="require(`./assets/headshot.jpg`)"
          transition="scale-transition"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
        Connor Moynahan
      </div>

      <v-spacer></v-spacer> -->

      <!-- <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn> -->
      <!-- <router-link class="router-options" to="/">About</router-link> |
      <router-link class="router-options" to="/searchbgg">Search BGG</router-link> -->
      
    <!-- </v-app-bar> -->

    <v-content>
      <router-view/>
      <!-- <HelloWorld/> -->
    </v-content>
  </v-app>
</template>

<script>
// import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    // HelloWorld,
  },

  data: () => ({
    //
  }),
};
</script>

<style scoped>

.router-options {
  color: white;
  margin: 10px;
}

.headshot-navbar{
  border-radius: 50%;
  height: 40px;
  width: 40px;
}

</style>

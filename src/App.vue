<template>
    <v-app>
        <v-navigation-drawer v-model="showDrawer" absolute temporary id="main-nav-bar">
            <v-list-item>
                <v-list-item-avatar>
                    <v-img :src="require(`./assets/headshot.jpg`)"></v-img>
                </v-list-item-avatar>

                <v-list-item-content>
                    <v-list-item-title>Connor Moynahan</v-list-item-title>
                </v-list-item-content>
            </v-list-item>

            <v-divider class="ma-0"></v-divider>

            <v-list dense>

                <!-- <v-list-item
            v-for="item in items"
            :key="item.title"
            link
          > -->
                <v-list-item link to="/resume">
                  
                    <v-list-item-icon>
                        <v-icon>fa-file</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                        <v-list-item-title>Resume</v-list-item-title>
                    </v-list-item-content>
                    
                </v-list-item>
                <v-list-item link to="/aboutme">
                    <v-list-item-icon>
                        <v-icon>fa-file</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                        <v-list-item-title>About Me</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
                <v-list-item link to="/contact">
                    <v-list-item-icon>
                        <v-icon>fa-file</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                        <v-list-item-title>Contact</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
        <v-app-bar app color="#4682B4" dark>
            <v-app-bar-nav-icon @click="showDrawer = !showDrawer"></v-app-bar-nav-icon>
            <div class="d-flex align-center">
                <!-- <v-img
            alt="Headshot"
            class="shrink mr-2 headshot-navbar"
            contain
            :src="require(`./assets/headshot.jpg`)"
            transition="scale-transition"
          /> -->

                <v-img alt="logo" class="shrink mt-1 logo-class" contain
                    :src="require(`./assets/logo.svg`)" style="cursor: pointer;" width="50" @click="showDrawer = !showDrawer"/>
                <!-- <h3 style="margin-left:10px;">Connor Moynahan</h3> -->
            </div>

            <v-spacer></v-spacer>

             <v-btn href="https://www.linkedin.com/in/connor-moynahan-0a568698/" target="_blank" text>
                <!-- <span class="mr-2">Latest Release</span> -->
                <v-icon>fa-linkedin-square</v-icon>
            </v-btn>
                         <v-btn href="mailto:connor.moynahan@gmail.com" text>
                <!-- <span class="mr-2">Latest Release</span> -->
                <v-icon>fa-envelope</v-icon>
            </v-btn>
            <!--<router-link class="router-options" to="/">About</router-link> |
            <router-link class="router-options" to="/searchbgg">Search BGG</router-link> -->

        </v-app-bar>

        <v-content>
            <router-view />
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
    showDrawer: false,
        //     items: [
        //   { title: 'Home', icon: 'dashboard' },
        //   { title: 'About', icon: 'question_answer' },
        // ],
  }),
};
</script>

<style scoped>

html,body,h1,h2,h3,h4,h5,h6 {font-family: "Roboto", sans-serif}

.router-options {
  color: white;
  margin: 10px;
}

.headshot-navbar{
  border-radius: 50%;
  height: 40px;
  width: 40px;
}

#main-nav-bar{
  position:fixed;
  top:0;
  left:0;
  overflow-y:scroll;
}

</style>

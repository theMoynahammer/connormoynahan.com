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
                                <v-list-item link to="/technologies">
                    <v-list-item-icon>
                        <v-icon>fa-code</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                        <v-list-item-title>Technologies</v-list-item-title>
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
            </div>

            <v-spacer></v-spacer>

            <!-- <v-btn  text>
                <a id ="download-resume-link" href="/Connor Moynahan - Resume.pdf" download>
                <v-icon>mdi-download</v-icon>
                </a>
            </v-btn> -->
            <v-btn @click="dialogOpen = true" text>
                <!-- <span class="mr-2">Latest Release</span> -->
                <v-icon>mdi-information-outline</v-icon>
            </v-btn>
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

        <v-dialog
      v-model="dialogOpen"
      width="500"
    >
      <v-card>
        <v-card-title
          class="headline lighten-2 dialog-class"
          primary-title
        >
          About this site
        </v-card-title>

        <v-card-text>
          {{aboutThisSite}}
        </v-card-text>

        <!-- <v-divider></v-divider> -->

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="primary"
            text
            @click="dialogOpen = false"
          >
            Neat!
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>

        <v-content>
            <router-view />
            <!-- <HelloWorld/> -->
        </v-content>
    </v-app>
</template>

<script>
// import HelloWorld from './components/HelloWorld';
import aboutThisSite from './text/aboutThisSite';
export default {
  name: 'App',

  components: {
    // HelloWorld,
  },

  data: () => ({
    showDrawer: false,
    dialogOpen: false,
    aboutThisSite: aboutThisSite.text,
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

.dialog-class{
  background-color: #4682B4;
  color: white;
  margin-bottom: 5px;
}

#main-nav-bar{
  position:fixed;
  top:0;
  left:0;
  overflow-y:scroll;
}

</style>

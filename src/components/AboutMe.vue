<template>
    <v-container>
        <!-- <v-btn v-if="!isMobile" id="weaknesses-button" dark>My Weaknesses</v-btn>
        <v-row  justify="space-around">
            <v-col sm="6">
                <v-card class="about-me-card">
                    <v-card-title>
                        About Me
                        </v-card-title>
                        <v-card-text>
                            Placeholder text for right here.<br/>
                            I need to figure out what information is good to go here.
                            </v-card-text>
                </v-card>
                <v-card class="about-me-card">
                    <v-card-title>
                        About Me
                        </v-card-title>
                        <v-card-text>
                            Placeholder text for right here.<br/>
                            I need to figure out what information is good to go here.
                            </v-card-text>
                </v-card>
                </v-col>
                <v-col sm="6">
                <v-card class="about-me-card">
                    <v-card-title>
                        About Me
                        </v-card-title>
                        <v-card-text>
                            Placeholder text for right here.<br/>
                            I need to figure out what information is good to go here.
                            </v-card-text>
                </v-card>
                <v-card class="about-me-card">
                    <v-card-title>
                        About Me
                        </v-card-title>
                        <v-card-text>
                            Placeholder text for right here.<br/>
                            I need to figure out what information is good to go here.
                            </v-card-text>
                </v-card>
            </v-col>
        </v-row> -->

        <v-row>
            <v-col>

<v-expansion-panels>
    <v-expansion-panel
      v-for="(item,i) in aboutMeContent.listItems"
      :key="i"
    >
      <v-expansion-panel-header><b>{{item.title}}</b></v-expansion-panel-header>
      <v-expansion-panel-content>
        {{item.content}}
      </v-expansion-panel-content>
    </v-expansion-panel>
  </v-expansion-panels>

            </v-col>
        </v-row>
    </v-container>
</template>

<script>

import $ from 'jquery';
import aboutMeContent from '../text/aboutMe';

export default {
    name: 'AboutMe',
    data: () => ({
        aboutMeContent,
    }),
    methods: {
         isMobile() {
   if(/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
     return true
   } else {
     return false
   }
    }
    },
    mounted() {
        $(document).ready(function() {
            const weaknessesButton = $("#weaknesses-button");

            const randomizeAnimation = () => {
                        var randX = Math.floor(Math.random() * (window.innerWidth - 100));
            var randY = Math.floor(Math.random() * (window.innerHeight - 100));
            console.log([randX, randY]);
            weaknessesButton.stop().animate({ "left": randX + "px", "top": randY + "px" });
        }
        weaknessesButton.on('mouseenter', randomizeAnimation);
        // weaknessesButton.on('mouseover', randomizeAnimation);
        // weaknessesButton.on('click', randomizeAnimation);
        weaknessesButton.on('touchstart', randomizeAnimation);
        });
    }
};
</script>

<style scoped>
.helper-text {
  color: #007bff;
}
html,body,h1,h2,h3,h4,h5,h6 {font-family: "Roboto", sans-serif}

.left-info-override{
    padding-top: 10px;
}

.text-light-blue{
    color: #4682B4;
}

.about-me-card{
    margin-bottom: 10px;
}

#weaknesses-button{
    position: relative;
    z-index: 2;  
}
</style>

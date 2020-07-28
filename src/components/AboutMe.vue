<template>
    <v-container>
        <v-btn id="weaknesses-button" dark>My Weaknesses</v-btn>
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
        </v-row>
    </v-container>
</template>

<script>

import $ from 'jquery';

export default {
    name: 'AboutMe',
    data: () => ({
    }),
    methods: {
        // animateButton() {
        //     var randX = Math.floor(Math.random() * (window.innerWidth - 100));
        //     var randY = Math.floor(Math.random() * (window.innerHeight - 100));
        //     console.log([randX, randY]);
        //     this.weaknessesButton.stop().animate({ "left": randX + "px", "top": randY + "px" });
        // }
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

<template>
    <v-container>
        <v-row  justify="space-around">
            <v-column>
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
                <v-card class="about-me-card">
                    <v-card-title>
                        About Me
                        </v-card-title>
                        <v-card-text>
                            Placeholder text for right here.<br/>
                            I need to figure out what information is good to go here.
                            </v-card-text>
                </v-card>
            </v-column>
        </v-row>
    </v-container>
</template>

<script>
export default {
  name: 'AboutMe',
  data: () => ({
  }),
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
</style>

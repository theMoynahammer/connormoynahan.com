<template>
    <v-container>
        <v-row  justify="space-around">
            <v-col>
                <v-card width="100%">
                    <v-card-title>
                        Contact Me
                        </v-card-title>
                        <v-card-text>
                            Hit me up.
                            </v-card-text>
                </v-card>
            </v-col>
                        <!-- <v-col>
                <v-card width="100%">
                    <v-card-title>
                        I dont know what should go here
                        </v-card-title>
                </v-card>
            </v-col> -->
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
</style>

<template>
    <v-container>
        <h2 class="w3-text-grey">Contact Info</h2>
        <v-row  justify="space-around">
            <v-col sm="6">
                <v-card class="card-style">
                    <v-card-title>
                        <v-icon class="icon-style">fa-envelope-o</v-icon>Email
                        </v-card-title>
                        <v-card-subtitle>connor.moynahan@gmail.com</v-card-subtitle>
                        <v-card-text>
                            Preferred method for communication.
                            </v-card-text>
                            <v-card-actions>
                                <v-spacer></v-spacer>
                                <v-btn href="mailto:connor.moynahan@gmail.com">Email Me</v-btn>
                            </v-card-actions>
                </v-card>
                <v-card class="card-style">
                    <v-card-title>
                        <v-icon class="icon-style">fa-phone</v-icon>Cell Phone
                        </v-card-title>
                        <v-card-subtitle>703-994-1421</v-card-subtitle>
                        <v-card-text>
                            Feel free to call or text me.
                            </v-card-text>
                            <v-card-actions>
                                <v-spacer></v-spacer>
                                <v-btn href="tel:703-994-1421">Call Me</v-btn>
                            </v-card-actions>
                </v-card>
                
            </v-col>
            <v-col sm="6">
                <v-card class="card-style">
                    <v-card-title>
                        <v-icon class="icon-style">fa-linkedin-square</v-icon>Connect on LinkedIn
                        </v-card-title>
                        <v-card-subtitle>https://www.linkedin.com/in/connor-moynahan-0a568698/</v-card-subtitle>
                        <v-card-text>
                            Recently updated my LinkedIn profile after years of dormancy.
                            </v-card-text>
                            <v-card-actions>
                                <v-spacer></v-spacer>
                                <v-btn href="https://www.linkedin.com/in/connor-moynahan-0a568698/" target="_blank" rel="noopener noreferrer">Go to my LinkedIn</v-btn>
                            </v-card-actions>
                </v-card>
                <v-card class="card-style">
                    <v-card-title>
                        <v-icon class="icon-style">fa-download</v-icon>Download my resume
                        </v-card-title>
                        <v-card-subtitle>This is up to date as of July 2020.</v-card-subtitle>
                        <v-card-text>
                            Want to read my resume offline? Here's your chance.
                            </v-card-text>
                            <v-card-actions>
                                <v-spacer></v-spacer>
                                <v-btn href="/Connor Moynahan - Resume 072020.pdf" download>Download my resume</v-btn>
                            </v-card-actions>
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

.card-style{
    margin-bottom: 10px;
}

.icon-style{
    margin-right: 10px;
}
</style>

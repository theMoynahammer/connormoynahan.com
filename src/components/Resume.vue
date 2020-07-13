<template>
    <v-container>
        <!-- <div class="search">
            <h1>Search for a board game</h1>
            <v-row>
                <v-col cols="12" sm="6" md="3">
                    <v-text-field color="#FF6347" v-model="searchInput" label="Search BoardGameGeek" outlined clearable
                        height="25" append-icon="mdi-magnify" @keyup.enter="search"></v-text-field>
                </v-col>
                <v-col>
                    <v-btn color="#FF6347" @click="search" height="56px">Search</v-btn>
                </v-col>
            </v-row>
            <v-col>
                <span v-show="searchHasHappened"><strong>{{numberOfResponses}} results</strong></span>
                <ul style="list-style-type:none;">
                    <li v-for="(result, index) in searchResponse" :key="index">
                        <a :href="`https://boardgamegeek.com/boardgame/${result['$'].id}`" target="_blank"
                            rel="noopener noreferrer">
                            {{result.name[0]['$'].value}}
                        </a>
                    </li>
                </ul>
            </v-col>
        </div> -->
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
<link rel='stylesheet' href='https://fonts.googleapis.com/css?family=Roboto'>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<!-- Page Container -->
<div class="w3-content w3-margin-top" style="max-width:1400px;">

  <!-- The Grid -->
  <div class="w3-row-padding">
  
    <!-- Left Column -->
    <div class="w3-third">
    
      <div class="w3-white w3-text-grey w3-card-4">
        <div class="w3-display-container">
          <img :src="require(`../assets/headshot-full.jpg`)" style="width:100%" alt="Avatar">
          <!-- <div class="w3-display-bottomleft w3-container w3-text-black">
            <h2>Jane Doe</h2>
          </div> -->
        </div>
        <div class="w3-container left-info-override">
            <p><i class="fa fa-user-o fa-fw w3-margin-right w3-large text-light-blue"></i><strong>Connor Moynahan</strong></p>
          <p><i class="fa fa-briefcase fa-fw w3-margin-right w3-large text-light-blue"></i>Full Stack Engineer/</p>
          <p><i class="fa fa-home fa-fw w3-margin-right w3-large text-light-blue"></i>Richmond, VA</p>
          <p><i class="fa fa-envelope fa-fw w3-margin-right w3-large text-light-blue"></i>connor.moynahan@gmail.com</p>
          <p><i class="fa fa-phone fa-fw w3-margin-right w3-large text-light-blue"></i>703-994-1421</p>
          <hr>

          <p class="w3-large"><b><i class="fa fa-code fa-fw w3-margin-right text-light-blue"></i>Technologies</b></p>
          <!-- <p>Adobe Photoshop</p> -->
          <h5>Proficient</h5>
          <ul>
              <li>testing</li>
              <li>ok</li>
          </ul>
                    <h5>Familiar</h5>
          <ul>
              <li>testing</li>
              <li>ok</li>
          </ul>
          
          <!-- <div class="w3-light-grey w3-round-xlarge w3-small">
            <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:90%">90%</div>
          </div>
          <p>Photography</p>
          <div class="w3-light-grey w3-round-xlarge w3-small">
            <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:80%">
              <div class="w3-center w3-text-white">80%</div>
            </div>
          </div>
          <p>Illustrator</p>
          <div class="w3-light-grey w3-round-xlarge w3-small">
            <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:75%">75%</div>
          </div>
          <p>Media</p>
          <div class="w3-light-grey w3-round-xlarge w3-small">
            <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:50%">50%</div>
          </div> -->
          <br>

          <!-- <p class="w3-large w3-text-theme"><b><i class="fa fa-globe fa-fw w3-margin-right text-light-blue"></i>Languages</b></p>
          <p>English</p>
          <div class="w3-light-grey w3-round-xlarge">
            <div class="w3-round-xlarge w3-teal" style="height:24px;width:100%"></div>
          </div>
          <p>Spanish</p>
          <div class="w3-light-grey w3-round-xlarge">
            <div class="w3-round-xlarge w3-teal" style="height:24px;width:55%"></div>
          </div>
          <p>German</p>
          <div class="w3-light-grey w3-round-xlarge">
            <div class="w3-round-xlarge w3-teal" style="height:24px;width:25%"></div>
          </div>
          <br> -->
        </div>
      </div><br>

    <!-- End Left Column -->
    </div>

    <!-- Right Column -->
    <div class="w3-twothird">
        
<div class="w3-container w3-card w3-white w3-margin-bottom">
        <h2 class="w3-text-grey">Overview</h2>
        <div class="w3-container">
            <p>This is where I will put my summary</p>
          <!-- <h5 class="w3-opacity"><img :src="require(`../assets/ge-logo.png`)" style="width:30px;margin-right:5px;" alt="Avatar"><b>General Electric / Staff Software Engineer</b></h5>
          <h6 class="text-light-blue"><i class="fa fa-calendar fa-fw w3-margin-right"></i>Jan 2019 - <span class="w3-tag w3-teal w3-round">Current</span></h6>
          <p>Lorem ipsum dolor sit amet. Praesentium magnam consectetur vel in deserunt aspernatur est reprehenderit sunt hic. Nulla tempora soluta ea et odio, unde doloremque repellendus iure, iste.</p>
          <hr> -->
        </div>
      </div>

      <div class="w3-container w3-card w3-white w3-margin-bottom">
        <h2 class="w3-text-grey w3-padding-16"><i class="fa fa-suitcase fa-fw w3-margin-right w3-xxlarge text-light-blue"></i>Work Experience</h2>
        <div class="w3-container">
          <h5 class="w3-opacity"><img :src="require(`../assets/ge-logo.png`)" style="width:30px;margin-right:5px;" alt="Avatar"><b>General Electric / Staff Software Engineer</b></h5>
          <h6 class="text-light-blue"><i class="fa fa-calendar fa-fw w3-margin-right"></i>Jan 2019 - <span class="w3-tag w3-teal w3-round">Current</span></h6>
          <p>Lorem ipsum dolor sit amet. Praesentium magnam consectetur vel in deserunt aspernatur est reprehenderit sunt hic. Nulla tempora soluta ea et odio, unde doloremque repellendus iure, iste.</p>
          <hr>
        </div>
        <div class="w3-container">
          <h5 class="w3-opacity"><img :src="require(`../assets/capitalone-logo.png`)" style="width:40px;margin-right:5px;" alt="Avatar"><b>Web Developer / something.com</b></h5>
          <h6 class="text-light-blue"><i class="fa fa-calendar fa-fw w3-margin-right"></i>Mar 2012 - Dec 2014</h6>
          <p>Consectetur adipisicing elit. Praesentium magnam consectetur vel in deserunt aspernatur est reprehenderit sunt hic. Nulla tempora soluta ea et odio, unde doloremque repellendus iure, iste.</p>
          <hr>
        </div>
        <div class="w3-container">
          <h5 class="w3-opacity"><b>Graphic Designer / designsomething.com</b></h5>
          <h6 class="text-light-blue"><i class="fa fa-calendar fa-fw w3-margin-right"></i>Jun 2010 - Mar 2012</h6>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. </p><br>
        </div>
      </div>

      <div class="w3-container w3-card w3-white">
        <h2 class="w3-text-grey w3-padding-16"><i class="fa fa-graduation-cap fa-fw w3-margin-right w3-xxlarge text-light-blue"></i>Education</h2>
        <div class="w3-container">
          <h5 class="w3-opacity"><b>W3Schools.com</b></h5>
          <h6 class="text-light-blue"><i class="fa fa-calendar fa-fw w3-margin-right"></i>Forever</h6>
          <p>Web Development! All I need to know in one place</p>
          <hr>
        </div>
        <div class="w3-container">
          <h5 class="w3-opacity"><b>London Business School</b></h5>
          <h6 class="text-light-blue"><i class="fa fa-calendar fa-fw w3-margin-right"></i>2013 - 2015</h6>
          <p>Master Degree</p>
          <hr>
        </div>
        <div class="w3-container">
          <h5 class="w3-opacity"><b>School of Coding</b></h5>
          <h6 class="text-light-blue"><i class="fa fa-calendar fa-fw w3-margin-right"></i>2010 - 2013</h6>
          <p>Bachelor Degree</p><br>
        </div>
      </div>

    <!-- End Right Column -->
    </div>
    
  <!-- End Grid -->
  </div>
  
  <!-- End Page Container -->
</div>

<!-- <footer class="w3-container w3-teal w3-center w3-margin-top">
  <p>Find me on social media.</p>
  <i class="fa fa-facebook-official w3-hover-opacity"></i>
  <i class="fa fa-instagram w3-hover-opacity"></i>
  <i class="fa fa-snapchat w3-hover-opacity"></i>
  <i class="fa fa-pinterest-p w3-hover-opacity"></i>
  <i class="fa fa-twitter w3-hover-opacity"></i>
  <i class="fa fa-linkedin w3-hover-opacity"></i>
  <p>Powered by <a href="https://www.w3schools.com/w3css/default.asp" target="_blank">w3.css</a></p>
</footer> -->

    </v-container>
</template>

<script>
import axios from 'axios';  
import xml2js from 'xml2js';

export default {
  name: 'SearchBgg',
  data: () => ({
    searchInput: null,
    searchResponse: null,
    numberOfResponses: null,
    searchHasHappened: false,
  }),
  methods: {
    search(){
      const baseBggUrl = "https://www.boardgamegeek.com/xmlapi2/";
      const searchBggUrl = `${baseBggUrl}search?type=boardgame,boardgameexpansion&query=`;

      axios.
        get(`${searchBggUrl}${this.searchInput}`)
        .then(({data: responseData}) => {
           return xml2js.parseStringPromise(responseData)
          // this.searchResponse = .toJson(responseAsXml);
        })
        .then((parsedAsJson)=>{
          console.log(parsedAsJson)
          this.searchHasHappened = true,
          this.numberOfResponses = parsedAsJson.items['$'].total;
          this.searchResponse = parsedAsJson.items.item;
          console.log('VVVVVVvvvvVVVV')
          console.log(JSON.parse(JSON.stringify(this.searchResponse)))
        })
        .catch((err)=>{
          alert(err)
        })
      // We save this URL for subsequent API calls
      // this.url = `https://fss.stage.gecompany.com/fss/pf-ws/authn/flows/${flowId}`;
      // axios
      //   .get(this.url, axiosOptions)
      //   .then(response => {
      //     this.lastResponse= JSON.stringify({...response.data, ...{httpStatus: response.status}});
      //     this.lastRequest=JSON.stringify(response.config)
      //     this.currentState = 'getStatus';
      //   })
    }
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
</style>

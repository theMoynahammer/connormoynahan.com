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
        <!-- Page Container -->
        <div class="w3-content w3-margin-top" style="max-width:1400px;">

            <!-- The Grid -->
            <div class="w3-row-padding">
                <div class="w3-container w3-card w3-white w3-margin-bottom custom-padding-overview">
                    <h2 class="w3-text-grey">Connor Moynahan</h2>
                    <div class="w3-container">
                        <p>{{summaryText}}</p>
                        <!-- <h5 class="w3-opacity"><img src="/assets/ge-logo.png" style="width:30px;margin-right:5px;" alt="Avatar"><b>General Electric / Staff Software Engineer</b></h5>
          <h6 class="text-light-blue"><i class="fa fa-calendar fa-fw w3-margin-right"></i>Jan 2019 - <span class="w3-tag w3-teal w3-round">Current</span></h6>
          <p>Lorem ipsum dolor sit amet. Praesentium magnam consectetur vel in deserunt aspernatur est reprehenderit sunt hic. Nulla tempora soluta ea et odio, unde doloremque repellendus iure, iste.</p>
          <hr> -->
                    </div>
                </div>
                <!-- Left Column -->
                <div class="w3-third">

                    <div class="w3-white w3-text-grey w3-card-4">
                        <div class="w3-display-container">
                            <img src="/assets/headshot-full.jpg" style="width:100%" alt="Avatar">
                            <!-- <div class="w3-display-bottomleft w3-container w3-text-black">
            <h2>Jane Doe</h2>
          </div> -->
                        </div>
                        <div class="w3-container left-info-override">
                            <!-- <p><i class="fa fa-user-o fa-fw w3-margin-right w3-large text-light-blue"></i><strong>Connor Moynahan</strong></p> -->
                            <!-- <p><i class="fa fa-briefcase fa-fw w3-margin-right w3-large text-light-blue"></i>Full Stack Engineer / Problem Solver</p> -->
                            <p><i class="fa fa-home fa-fw w3-margin-right w3-large text-light-blue"></i>Richmond, VA</p>
                            <p><a href="mailto:connor.moynahan@gmail.com"><i
                                        class="fa fa-envelope fa-fw w3-margin-right w3-large text-light-blue"></i>connor.moynahan@gmail.com</a>
                            </p>
                            <p><a href="tel:703-994-1421"><i
                                        class="fa fa-phone fa-fw w3-margin-right w3-large text-light-blue"></i>703-994-1421</a>
                            </p>
                            <p> <a href="/Connor Moynahan - updated 9_2021.pdf" download><i
                                        class="fa fa-download fa-fw w3-margin-right w3-large text-light-blue"></i>Download
                                    Resume</a></p>

                            <hr class="custom-hr">

                            <p class="w3-large margin-bottom-0-class"><b><i
                                        class="fa fa-code fa-fw w3-margin-right text-light-blue padding-overwrite"></i>Languages/Technologies</b>
                            </p>
                            <!-- <p>Adobe Photoshop</p> -->
                            <!-- <h5>Proficient</h5> -->
                            <v-container>
                                        <v-row>
                                            <v-col sm="6">
                            <div class="skills-section" v-for="skill in proficientSkills.slice(0, 8)" :key="skill.name">
                                <!-- <div class="tech-skill"> -->
                                <!-- <p class="display-inline-block"> -->
                                    
                                            
                                            
                                        
                                <v-img class="tech-logo" :src="skill.logo"></v-img>{{ skill.name }}
                                
                                <!-- </p> -->
                                <!-- </div> -->
                            </div>
                            </v-col>
                                <v-col sm="6">
                                    <div class="skills-section" v-for="skill in proficientSkills.slice(8, 16)" :key="skill.name">
                                <!-- <div class="tech-skill"> -->
                                <!-- <p class="display-inline-block"> -->
                                    
                                            
                                            
                                        
                                <v-img class="tech-logo" :src="skill.logo"></v-img>{{ skill.name }}
                                
                                <!-- </p> -->
                                <!-- </div> -->
                            </div>
                                            </v-col>
                                </v-row>
                                        </v-container>
                                        <hr class="custom-hr">
                            <p class="w3-large"><b><i
                                        class="fa fa-certificate fa-fw w3-margin-right text-light-blue padding-overwrite"></i>Certifications</b>
                            </p>
                            <div class="skills-section">
                                <v-img class="tech-logo" src="/assets/tech-logos/exam-az300-600x600.png"></v-img>AZ-300 Microsoft Azure Architect Technologies Exam - Nov 2019
                                </div>
                            <!-- <ul>
                <li v-for="skill in proficientSkills" :key="skill.name">
                    <v-img style="height:10px;width: 10px;" :src="skill.logo"></v-img>{{ skill.name }}
                </li>
          </ul>
                    <h5>Familiar</h5>
          <ul>
              <li>testing</li>
              <li>ok</li>
          </ul> -->

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
                        <h2 class="w3-text-grey padding-overwrite">
                          <!-- <i
                                class="fa fa-suitcase fa-fw w3-margin-right w3-xxlarge text-light-blue"></i> -->
                                Work Experience as of 12/2020(View resume for up to date experience)</h2>
                        <div class="w3-container">
                            <h5 class="w3-opacity margin-top-0"><img src="/assets/ge-logo.png" style="width:30px;margin-right:5px;"
                                    alt="Avatar"><b><span class="italics">General Electric,</span> Staff Software
                                    Engineer - Identity Team</b></h5>
                            <h6 class="text-light-gray">Jan 2019 -
                                <span class="w3-tag background-light-blue w3-round">Current</span></h6>
                            <!-- <p>Lorem ipsum dolor sit amet. Praesentium magnam consectetur vel in deserunt aspernatur est reprehenderit sunt hic. Nulla tempora soluta ea et odio, unde doloremque repellendus iure, iste.</p> -->
                            <ul v-for="(item, index) in workExperienceJson.ge" :key="index">
                                <li>{{item}}</li>
                            </ul>
                            <hr>
                        </div>
                        <div class="w3-container">
                            <h5 class="w3-opacity margin-top-0"><img src="/assets/capitalone-logo.png"
                                    style="width:30px;margin-right:5px;" alt="Avatar"><b><span class="italics">Capital
                                        One,</span> Senior Software Engineer - Small Business</b></h5>
                            <h6 class="text-light-gray">Sep 2018 -
                                Jan 2019</h6>
                                <!-- <i class="fa fa-calendar fa-fw w3-margin-right"></i> -->
                            <!-- <p>Consectetur adipisicing elit. Praesentium magnam consectetur vel in deserunt aspernatur est reprehenderit sunt hic. Nulla tempora soluta ea et odio, unde doloremque repellendus iure, iste.</p> -->
                            <ul v-for="(item, index) in workExperienceJson.capOneSmallBusiness" :key="index">
                                <li>{{item}}</li>
                            </ul>
                            <hr>
                        </div>
                        <div class="w3-container">
                            <h5 class="w3-opacity margin-top-0"><img src="/assets/capitalone-logo.png"
                                    style="width:30px;margin-right:5px;" alt="Avatar"><b><span class="italics">Capital
                                        One,</span> Senior Software Engineer - Consumer Card</b></h5>
                            <h6 class="text-light-gray">Feb 2014 -
                                Aug 2018</h6>
                            <!-- <p>Consectetur adipisicing elit. Praesentium magnam consectetur vel in deserunt aspernatur est reprehenderit sunt hic. Nulla tempora soluta ea et odio, unde doloremque repellendus iure, iste.</p> -->
                            <ul v-for="(item, index) in workExperienceJson.capOneCard" :key="index">
                                <li>{{item}}</li>
                            </ul>
                            <hr>
                        </div>
                        <div class="w3-container">
                            <h5 class="w3-opacity margin-top-0"><img src="/assets/capitalone-logo.png"
                                    style="width:30px;margin-right:5px;" alt="Avatar"><b><span class="italics">Capital
                                        One,</span> Testing Specialist</b></h5>
                            <h6 class="text-light-gray">Jul 2012 -
                                Jan 2014</h6>
                            <ul v-for="(item, index) in workExperienceJson.capOneQa" :key="index">
                                <li>{{item}}</li>
                            </ul>
                            <hr>
                        </div>
                        <div class="w3-container margin-bottom-class">
                            <h5 class="w3-opacity margin-top-0"><img src="/assets/capitalone-logo.png"
                                    style="width:30px;margin-right:5px;" alt="Avatar"><b><span class="italics">Capital
                                        One,</span> Process Manager - Tech Development Program</b></h5>
                            <h6 class="text-light-gray">Jul 2011 - Jul 2012</h6>
                            <ul v-for="(item, index) in workExperienceJson.capOneProcess" :key="index">
                                <li>{{item}}</li>
                            </ul>
                        </div>
                    </div>

                    <div class="w3-container w3-card w3-white">
                        <h2 class="w3-text-grey padding-overwrite">
                          <!-- <i
                                class="fa fa-graduation-cap fa-fw w3-margin-right w3-xxlarge text-light-blue"></i> -->
                                Education
                        </h2>
                        <div class="w3-container">
                            <h5 class="w3-opacity margin-top-0"><img src="/assets/vt-logo.svg" style="height:20px;margin-right:10px;"
                                    alt="Avatar"><b>B.S. Business Information Technology</b></h5>
                            <h6 class="text-light-gray">2007 - 2011
                            </h6>
                            <!-- <p>{{workExperienceJson.bitInfo}}</p> -->
                            <!-- <hr> -->
                        </div>
                        <!-- <div class="w3-container">
          <h5 class="w3-opacity"><b>London Business School</b></h5>
          <h6 class="text-light-blue"><i class="fa fa-calendar fa-fw w3-margin-right"></i>2013 - 2015</h6>
          <p>Master Degree</p>
          <hr>
        </div>
        <div class="w3-container">
          <h5 class="w3-opacity"><b>School of Coding</b></h5>
          <h6 class="text-light-blue"><i class="fa fa-calendar fa-fw w3-margin-right"></i>2010 - 2013</h6>
          <p>Bachelor Degree</p><br>
        </div> -->
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
import summaryText from '../text/summary';
import technicalSkills from '../text/technicalSkills';
import workExperienceJson from '../text/workExperience';

export default {
  name: 'SearchBgg',
  data: () => ({
    searchInput: null,
    searchResponse: null,
    numberOfResponses: null,
    searchHasHappened: false,
    summaryText: summaryText.text,
    proficientSkills: technicalSkills.proficient,
    workExperienceJson,
  }),
  methods: {
      getImgUrl(url){
          return require(url)
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

.tech-logo{
      display: block;
  max-width:15px;
  width: auto;
  height: auto;
  display: inline-block;
  margin-right: 5px;
}

.custom-hr{
    margin-top: 10px;
    margin-bottom: 10px;
}

.italics{
  font-style: italic;
}

.padding-overwrite {
  padding-bottom: 0px;
  padding-top: 16px;
}

.skills-section{
    margin-left:15px;
}

.margin-bottom-class{
  margin-bottom: 20px;
}

.margin-bottom-0-class{
    margin-bottom: 0px;
}

.display-inline-block{
    display: inline-block;
}

#download-resume-link{
  text-decoration: none; 
  /* color: white; */
}

.text-light-blue{
    color: #4682B4;
}

.background-light-blue{
    background-color: #4682B4;
}

.text-light-gray{
    color: #757575;
}

.custom-padding-overview{
    margin: 0px 8px;
}

.tech-skill{
    display: inline;
}

.margin-top-0{
  margin-top: 0px;
}
</style>

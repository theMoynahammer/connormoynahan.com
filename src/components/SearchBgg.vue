<template>
<v-container>
  <div class="search">
    <h1>Search for a board game</h1>
<v-row>
        <v-col cols="12" sm="6" md="3">
          <v-text-field
            color="#FF6347"
            v-model="searchInput"
            label="Search BoardGameGeek"
            outlined
            clearable
            height="25"
            append-icon="mdi-magnify"
            @keyup.enter="search"
          ></v-text-field>
        </v-col>
        <v-col>
          <v-btn
          color="#FF6347"
          @click="search"
          height="56px">Search</v-btn>
        </v-col>
</v-row>
<v-col>
  <span v-show="searchHasHappened"><strong>{{numberOfResponses}} results</strong></span>
  <ul style="list-style-type:none;">
    <li v-for="(result, index) in searchResponse" :key="index">
      <a :href="`https://boardgamegeek.com/boardgame/${result['$'].id}`" target="_blank" rel="noopener noreferrer">
        {{result.name[0]['$'].value}}
        </a>
    </li>
  </ul>
</v-col>
  </div>
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
</style>

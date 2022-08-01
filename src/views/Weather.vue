
<template>
  <div class="weather">
    <h1>hallloooooiiiiiiiii</h1>
    <p>Lets try to make an API call</p>
    <p>You can choose your city first:</p>
    <button @click="getWeather" class="apibutton">TESTBUTTON 4 the API</button>

    <div id="app">
      {{ info }}
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  el: '#app',
  name: "Weather",
  data() {
    return {
      info: null
    };
  },
  methods: {
    getWeather() {
      const api_key = process.env.VUE_APP_API_KEY
      axios
          .get('https://api.weatherapi.com/v1/current.json?key=' + api_key + '&q=Cologne')
          .then(response => (this.info = response))
          .catch(error => console.log(error))
      //console.log(process.env.VUE_APP_API_KEY)
    },
    xyinja1() {
      const api_key = process.env.VUE_APP_API_KEY
      axios
          .get('https://api.weatherapi.com/v1/current.json?key=' + api_key + '&q=Cologne')
          .then(response => (this.info = response))
          .catch(error => console.log(error))
      //console.log(process.env.VUE_APP_API_KEY)

    }
  }
}



/*
new Vue({
  
});
*/


/*
//https://zetcode.com/javascript/axios/ axios stuff
const axios = require('axios');

async function makeRequest() {

  const config = {
    method: 'get',
    url: process.env.API_CALL
    //process.env.API_CALL
  }

  let res = await axios(config)

  console.log(res);
}

makeRequest();*/
</script>

<style scoped>
#app {
  padding-top: 55px;
  background: aqua;
}

.weather {
  background: #42b983;
}

.background {
  background: #42b983;
}
</style>
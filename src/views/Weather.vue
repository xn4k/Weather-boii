
<template>
  <div class="weather">
    <h1>hallloooooiiiiiiiii</h1>
    <p>Lets try to make an API call</p>
    <button class="apibutton">TESTBUTTON 4 the API</button>

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
  mounted() {
    axios
        .get('https://api.weatherapi.com/v1/current.json?key=ffc4143944e6422ab0602017221806&q=Cologne')
        .then(response => (this.info = response));
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
}
</style>
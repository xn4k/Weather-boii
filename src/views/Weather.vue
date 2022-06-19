
<template>
  <div class="weather">
    <h1>hallloooooiiiiiiiii</h1>
    <p>Lets try to make an API call</p>
    <button class="apibutton">TESTBUTTON 4 the API</button>
    <p></p>



  </div>
</template>

<script>
export default {
  name: "Weather"
}
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

makeRequest();
</script>

<style scoped>

</style>